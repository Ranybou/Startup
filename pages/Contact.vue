<template>
  <form>
    <div class="space-y-12 text-center">
      <div class="border-b border-zinc-900/10 pb-12 text-center">
        <h2 class="font-bold text-3xl leading-7 text-zinc-950">
          <i class="font-bold text-3xl ri-user-fill"></i> Contactez-nous !
        </h2>
        <p class="mt-1 text-sm leading-6 text-black text-center">
          Ces informations vont être affichées publiquement, donc faites
          attention aux informations que vous partagez.
        </p>

        <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8">
          <div class="sm:col-span-4">
            <label
              for="nom"
              class="block text-sm font-medium leading-6 text-zinc-950 text-center"
              >Nom</label
            >
            <div class="mt-2">
              <div
                class="flex rounded-md shadow-sm ring-1 ring-inset ring-black focus-within:ring-2 focus-within:ring-inset focus-within:ring-indigo-600 sm:max-w-md"
              >
                <input 
                  type="text"
                  name="nom"
                  id="nom"
                  autocomplete="nom"
                  class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-zinc-950 placeholder:text-black focus:ring-0 sm:text-sm sm:leading-6 "
                  placeholder="Bouhlila"
                />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8">
        <div class="sm:col-span-4">
          <label
            for="prenom"
            class="block text-sm font-medium leading-6 text-zinc-950 text-center"
            >Prénom</label
          >
          <div class="mt-2">
            <div
              class="flex rounded-md shadow-sm ring-1 ring-inset ring-black focus-within:ring-2 focus-within:ring-inset focus-within:ring-indigo-600 sm:max-w-md"
            >
              <input
                type="text"
                name="prenom"
                id="prenom"
                autocomplete="prenom"
                class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-zinc-950 placeholder:text-black focus:ring-0 sm:text-sm sm:leading-6"
                placeholder="Rany"
              />
            </div>
          </div>
        </div>

        <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8">
          <div class="border-b border-black/10 pb-2"></div>
          <div class="sm:col-span-4 text-center">
            <label
              for="email"
              class="block text-sm font-medium leading-6 text-zinc-950 text-center"
              >E-mail</label
            >
            <div class="mt-2">
              <div
                class="flex rounded-md shadow-sm ring-1 ring-inset ring-black focus-within:ring-2 focus-within:ring-inset focus-within:ring-indigo-600 sm:max-w-md"
              >
                <input
                  type="email"
                  name="email"
                  id="email"
                  autocomplete="email"
                  class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-zinc-950 placeholder:text-black focus:ring-0 sm:text-sm sm:leading-6"
                  placeholder="exemple@demail.be"
                />
              </div>
            </div>
          </div>
          <div class="col-span-full">
            <label
              for="message"
              class="block text-sm font-medium leading-6 text-zinc-950 text-center"
              >Votre message</label
            >
            <div class="mt-2">
              <textarea
                id="message"
                name="message"
                rows="3"
                class="block w-full rounded-md border-0 py-1.5 text-zinc-950 shadow-sm ring-1 ring-inset ring-black placeholder:text-black focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
              />
            </div>
            <p class="mt-3 text-sm leading-6 text-black text-center">
              Ecrivez le message souhaité.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="mt-6 flex items-center justify-end gap-x-6">
      <button
        type="button"
        class="text-sm font-semibold leading-6 text-zinc-950"
      >
        Annuler
      </button>
      <button
        type="submit"
        class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
      >
        Envoyer
      </button>
    </div>
  </form>

</template>

<script setup></script>
