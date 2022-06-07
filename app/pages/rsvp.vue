<template>
  <section class="rsvp">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center">
      <div
        class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden markdown"
      >
        <h1>RSVP</h1>
      </div>
      <div class="flex flex-col w-full xl:w-2/5 markdown">
        <h4 v-if="isSignedUp">Thank you!</h4>

        <form v-else @submit.prevent="handleSubmit" name="rsvps" netlify>
          <div class="border border-grey-400 p-8 pt-4">
            <h2 class="pb-0">Please fill out to RSVP</h2>
            <div class="flex items-center border-b border-blue-400 py-2">
              <input
                ref="nameInput"
                v-model="form.name"
                class="appearance-none mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight focus:outline-none"
                type="text"
                name="name"
                placeholder="Your full name"
                aria-label="Your name"
              />
            </div>

            <div class="flex flex-col items-center border-b border-b-2 border-blue-400 py-2">
              <p class="pt-0 pb-4 text-gray-600">
                If you are attending both ceremony and reception in-person, please select all
                options that apply:
              </p>
              <p
                class="mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight"
              >
                <label for="ceremony"
                  ><input
                    class="mr-2"
                    type="checkbox"
                    id="ceremony"
                    name="ceremony"
                    v-model="form.ceremony"
                    @change="doCheck('ceremony')"
                  />Yes, I will attend the ceremony</label
                >
              </p>
              <p
                class="mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight"
              >
                <label for="reception"
                  ><input
                    class="mr-2"
                    type="checkbox"
                    id="reception"
                    name="reception"
                    v-model="form.reception"
                    @change="doCheck('reception')"
                  />Yes, I will attend the reception</label
                >
              </p>
              <p
                class="mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight"
              >
                <label for="streaming"
                  ><input
                    class="mr-2"
                    type="checkbox"
                    id="streaming"
                    name="streaming"
                    v-model="form.streaming"
                    @change="doCheck('streaming')"
                  />I will attend a virtual streaming of the ceremony</label
                >
              </p>
              <p
                class="mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight"
              >
                <label for="unableToAttend"
                  ><input
                    class="mr-2"
                    type="checkbox"
                    id="unableToAttend"
                    name="unableToAttend"
                    v-model="form.unableToAttend"
                    @change="doCheck('unableToAttend')"
                  />No, I will not be attending</label
                >
              </p>
            </div>

            <div v-if="isComingToEvent" class="flex flex-col border-b border-blue-400 py-2">
              <p class="pt-4 pb-1 text-gray-600">
                Are you bringing a +1 on the day?
              </p>
              <p
                class="mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight"
              >
                <label for="guest"
                  ><input
                    class="mr-2"
                    type="checkbox"
                    id="guest"
                    name="guest"
                    v-model="form.guest"
                    @change="doCheck('guest')"
                  />Yes, I will bring a guest</label
                >
              </p>
            </div>

            <div v-if="hasGuest" class="flex items-center border-b border-blue-400 py-2">
              <input
                ref="guestNameInput"
                v-model="form.guestName"
                class="appearance-none mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight focus:outline-none"
                type="text"
                name="guestName"
                placeholder="Your guest's full name"
                aria-label="Your guest's full name"
              />
            </div>

            <div class="flex items-center border-b border-blue-400 py-2">
              <input
                ref="emailInput"
                v-model="form.email"
                class="appearance-none mb-36 bg-transparent border-none w-full text-gray-700 mr-3 py-1 px-2 leading-tight focus:outline-none"
                type="text"
                name="email"
                placeholder="your@email.com"
                aria-label="Email address"
              />

              <button
                class="flex-shrink-0 bg-blue-500 hover:bg-blue-700 border-blue-500 hover:border-blue-700 text-sm border-4 text-white py-1 px-2 rounded"
                type="submit"
              >
                Send my RSVP
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})
export default class RSVP extends Vue {
  isSignedUp = false;

  isComingToEvent = false;

  hasGuest = false;

  form = [
    {
      ceremony: false,
      reception: false,
      streaming: false,
      unableToAttend: false,
      attendance: '',
      name: '',
      email: '',
      guest: false,
      guestName: '',
    },
  ];

  encode(data): string {
    return Object.keys(data)
      .map((key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`)
      .join('&');
  }

  doCheck(check: string): void {
    if (check === 'ceremony' || check === 'reception') {
      if (this.form.ceremony || this.form.reception) {
        this.form.unableToAttend = false;
        this.form.streaming = false;
        this.isComingToEvent = true;
      } else {
        this.isComingToEvent = false;
        this.hasGuest = false;
        this.form.guest = false;
        this.form.guestName = '';
      }
    }
    if (check === 'streaming') {
      if (this.form.streaming) {
        this.form.unableToAttend = false;
        this.form.ceremony = false;
        this.form.reception = false;
        this.form.guest = false;
        this.form.guestName = '';
        this.isComingToEvent = false;
        this.hasGuest = false;
      }
    }
    if (check === 'unableToAttend') {
      if (this.form.unableToAttend) {
        this.form.streaming = false;
        this.form.ceremony = false;
        this.form.reception = false;
        this.form.guest = false;
        this.form.guestName = '';
        this.isComingToEvent = false;
        this.hasGuest = false;
      }
    }
    if (check === 'guest') {
      if (this.form.guest) {
        this.hasGuest = true;
      } else {
        this.hasGuest = false;
        this.form.guestName = '';
      }
    }
  }

  validEmail(email): boolean {
    // eslint-disable-next-line
    const re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    return re.test(email);
  }

  async handleSubmit(): Promise<void> {
    if (!this.validEmail(this.form.email)) {
      this.$refs.emailInput.focus();
      return;
    }

    try {
      await fetch('/', {
        method: 'POST',
        headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
        body: this.encode({ 'form-name': 'rsvps', ...this.form }),
      });
      console.log(...this.form);
      this.isSignedUp = true;
    } catch (error) {
      console.error(error);
    }
  }
}
</script>
