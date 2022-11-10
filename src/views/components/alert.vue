<template>
  <!-- Search component Alert with name of type,  press Ctrl + F -->

  <div class="alert h-auto p-3">
    <nav class="flex" aria-label="Breadcrumb">
      <ol class="inline-flex items-center space-x-1 md:space-x-3">
        <li class="inline-flex items-center">
          <a
            href="#"
            class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white"
          >
            <svg
              class="mr-2 w-4 h-4"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
              ></path>
            </svg>
            Dashboard
          </a>
        </li>
        <li>
          <div class="flex items-center">
            <svg
              class="w-6 h-6 text-gray-400"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                clip-rule="evenodd"
              ></path>
            </svg>
            <a
              href="#"
              class="ml-1 text-sm font-medium text-gray-700 hover:text-gray-900 md:ml-2 dark:text-gray-400 dark:hover:text-white"
              >Components</a
            >
          </div>
        </li>
        <li>
          <div class="flex items-center">
            <svg
              class="w-6 h-6 text-gray-400"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                clip-rule="evenodd"
              ></path>
            </svg>
            <a
              href="#"
              class="ml-1 text-sm font-medium text-gray-700 hover:text-gray-900 md:ml-2 dark:text-gray-400 dark:hover:text-white"
              >Computer</a
            >
          </div>
        </li>
      </ol>
    </nav>
    <!-- end nav -->
    
    <div class="dark:bg-slate-900">
      <section
        id="login"
        class="p-4 flex flex-col justify-center min-h-screen max-w-md mx-auto"
      >
     
        <div class="p-6 bg-sky-100 dark:bg-slate-700 rounded">
          <div class="flex items-center justify-center font-black m-3 mb-12 flex-row">
            <h1 class="tracking-wide text-3xl dark:text-gray-300 text-gray-900">
              Add Computer
            </h1>
          </div>
          <form class="flex flex-col justify-center" @submit.prevent="submit">
            <div class="flex justify-between items-center mb-3">
              <div class="inline-flex items-center self-start">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-8 w-8 mr-3 bg-gradient-to-r from-pink-600 to-red-600 shadow-lg rounded p-1.5 dark:bg-slate-800 text-gray-100"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path d="M13 7H7v6h6V7z" />
                  <path
                    fill-rule="evenodd"
                    d="M7 2a1 1 0 012 0v1h2V2a1 1 0 112 0v1h2a2 2 0 012 2v2h1a1 1 0 110 2h-1v2h1a1 1 0 110 2h-1v2a2 2 0 01-2 2h-2v1a1 1 0 11-2 0v-1H9v1a1 1 0 11-2 0v-1H5a2 2 0 01-2-2v-2H2a1 1 0 110-2h1V9H2a1 1 0 010-2h1V5a2 2 0 012-2h2V2zM5 5h10v10H5V5z"
                    clip-rule="evenodd"
                  />
                </svg>
                <span class="font-bold text-gray-900 dark:text-gray-200"></span>
              </div>
            </div>
            <label class="text-sm font-medium dark:text-white text-gray-600"
              >Computer name</label
            >
            <input
              class="mb-3 px-2 py-1.5 mb-3 mt-1 block w-full px-2 py-1.5 border border-gray-300 rounded-md text-sm shadow-sm placeholder-gray-400 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 focus:invalid:border-red-500 focus:invalid:ring-red-500"
              type="text"
              name="title"
              placeholder="title..."
              v-model="title"
            />
            <label class="text-sm font-medium dark:text-white text-gray-600"
              >Computer description</label
            >
            <textarea
              cols="30"
              rows="10"
              class="mb-3 mt-1 block w-full px-2 py-1.5 border border-gray-300 rounded-md text-sm shadow-sm placeholder-gray-400 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 focus:invalid:border-red-500 focus:invalid:ring-red-500"
              name="messages"
              placeholder="content..."
              v-model="description"
            ></textarea>
            <button
              class="px-4 py-1.5 rounded-md shadow-lg bg-indigo-600 font-medium text-gray-100 block transition duration-300"
              type="submit"
            >
              <span class="hidden">Processing</span>
              <span class="dark:text-white">Add<span id="subtotal"></span></span>
            </button>
          </form>
          <ToggleMode />
        </div>
      </section>
    </div>
  </div>
 
  
  
</template>

<script>
  import { Icon } from "@iconify/vue";
  export default {
    components: {
      Icon,
    },
    mounted() {
      var alert_dis = document.querySelectorAll(".alert-dismiss");
      alert_dis.forEach((x) =>
        x.addEventListener("click", function () {
          x.parentElement.classList.add("hidden");
        })
      );
    },
  };
</script>
