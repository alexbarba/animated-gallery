<template>
  <div
    class="relative flex justify-center bg-white dark:bg-gray-900 sm:items-center sm:pt-0"
  >
    <div class="max-w-6xl mx-auto sm:px-6 lg:px-8">
      <div class="mt-8 overflow-hidden">
        <div class="grid grid-cols-1 md:grid-cols-2">
          <div class="p-6 mr-2 bg-gray-100 dark:bg-gray-800 sm:rounded-lg">
            <h1
              class="text-4xl sm:text-5xl text-gray-800 dark:text-white font-extrabold tracking-tight"
            >
              Subir imagen
            </h1>
            <p
              class="text-normal text-lg sm:text-2xl font-medium text-gray-600 dark:text-gray-400 mt-2"
            >
              Completa el formulario para mostrar tu imagen en nuestra galeria
              interactiva
            </p>
          </div>

          <form class="p-6 flex flex-col justify-center">
            <div class="flex flex-col">
              <label for="title" class="hidden">Titulo</label>
              <input
                id="title"
                type="title"
                name="title"
                placeholder="Titulo"
                class="w-100 mt-2 py-3 px-3 rounded-lg bg-white dark:bg-gray-800 border border-gray-400 dark:border-gray-700 text-gray-800 font-semibold focus:border-indigo-500 focus:outline-none"
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="description" class="hidden">Description</label>
              <input
                id="description"
                type="description"
                name="description"
                placeholder="Descripcion"
                class="w-100 mt-2 py-3 px-3 rounded-lg bg-white dark:bg-gray-800 border border-gray-400 dark:border-gray-700 text-gray-800 font-semibold focus:border-indigo-500 focus:outline-none"
              />
            </div>

            <div class="flex flex-col mt-2">
              <label for="url" class="hidden">Url</label>
              <input
                id="url"
                type="url"
                name="url"
                placeholder="Url"
                class="w-100 mt-2 py-3 px-3 rounded-lg bg-white dark:bg-gray-800 border border-gray-400 dark:border-gray-700 text-gray-800 font-semibold focus:border-indigo-500 focus:outline-none"
              />
            </div>

            <button
              type="submit"
              class="md:w-32 bg-indigo-600 hover:bg-blue-dark text-white font-bold py-3 px-6 rounded-lg mt-3 hover:bg-indigo-500 transition ease-in-out duration-300"
            >
              Cargar
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Form',
}
</script>

<style></style>
