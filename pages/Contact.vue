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
              class="block text-sm font-medium leading-6 text-zinc-950 flex items-center"
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
            class="block text-sm font-medium leading-6 text-zinc-950 flex items-center"
            >Prénom</label
          >
          <div class="mt-2">
            <div
              class="flex rounded-md shadow-sm ring-1 ring-inset ring-black focus-within:ring-2 focus-within:ring-inset focus-within:ring-indigo-600 sm:max-w-md flex items-center"
            >
              <input
                type="text"
                name="prenom"
                id="prenom"
                autocomplete="prenom"
                class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-zinc-950 placeholder:text-black focus:ring-0 sm:text-sm sm:leading-6 flex items-center"
                placeholder="Rany"
              />
            </div>
          </div>
        </div>

        <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8 flex items-center">
          <div class="border-b border-black/10 pb-2"></div>
          <div class="sm:col-span-4 text-center">
            <label
              for="email"
              class="block text-sm font-medium leading-6 text-zinc-950 flex items-center"
              >E-mail</label
            >
            <div class="mt-2">
              <div
                class="flex rounded-md shadow-sm ring-1 ring-inset ring-black focus-within:ring-2 focus-within:ring-inset focus-within:ring-indigo-600 sm:max-w-md flex items-center"
              >
                <input
                  type="email"
                  name="email"
                  id="email"
                  autocomplete="email"
                  class="block flex-1 border-0 bg-transparent py-1.5 pl-1 text-zinc-950 placeholder:text-black focus:ring-0 sm:text-sm sm:leading-6 flex items-center"
                  placeholder="exemple@demail.be"
                />
              </div>
            </div>
          </div>
          <div class="col-span-full">
            <label
              for="message"
              class="block text-sm font-medium leading-6 text-zinc-950 flex items-center"
              >Votre message</label
            >
            <div class="mt-2">
              <textarea
                id="message"
                name="message"
                rows="3"
                class="block w-full rounded-md border-0 py-1.5 text-zinc-950 shadow-sm ring-1 ring-inset ring-black placeholder:text-black focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6 flex items-center"
              />
            </div>
            <p class="mt-3 text-sm leading-6 text-black flex items-center">
              Ecrivez le message souhaité.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="mt-6 flex items-center gap-x-6">
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

 <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2526.1312435957193!2d4.605170176828972!3d50.71750427164439!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c17d7411704eef%3A0x30bbaf4d6d8a913b!2sRue%20de%20la%20Limite%206%2C%201300%20Wavre!5e0!3m2!1sfr!2sbe!4v1704666124298!5m2!1sfr!2sbe" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="flex items-center justify-end"></iframe>
 
</template>

<script setup></script>
