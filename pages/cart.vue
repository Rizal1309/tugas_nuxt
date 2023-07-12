<template>
  <Header></Header>
  <div>
    <section class="h-screen bg-gray-100 py-12 sm:py-16 lg:py-20 mt-0">
      <div class="mx-auto px-1 sm:px-6 lg:px-8">
        <div class="flex items-center justify-center"></div>

        <div class="mx-auto mt-8 max-w-md md:mt-12">
          <div class="rounded-3xl bg-white shadow-lg">
            <div class="px-4 py-6 sm:px-8 sm:py-10">
              <div class="flow-root">
                <ul class="-my-8">
                  <li
                    class="flex flex-col space-y-3 py-6 text-left sm:flex-row sm:space-x-5 sm:space-y-0"
                  >
                    <div class="shrink-0 relative">
                      <span
                        class="absolute top-1 left-1 flex h-6 w-6 items-center justify-center rounded-full border bg-white text-sm font-medium text-gray-500 shadow sm:-top-2 sm:-right-2"
                        >1</span
                      >
                      <img
                        class="h-24 w-24 max-w-full rounded-lg object-cover"
                        src="data:image/jpeg;base64,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"
                        alt=""
                      />
                    </div>

                    <div class="relative flex flex-1 flex-col justify-between">
                      <div class="sm:col-gap-5 sm:grid sm:grid-cols-2">
                        <div class="pr-8 sm:pr-5">
                          <p class="text-base font-semibold text-gray-900">
                            rendang sapi mak ijah
                          </p>
                          <p class="mx-0 mt-1 mb-0 text-sm text-gray-400">
                            anda puas? dompetpun malas
                          </p>
                        </div>

                        <div
                          class="mt-4 flex items-end justify-between sm:mt-0 sm:items-start sm:justify-end"
                        >
                          <p
                            class="shrink-0 w-20 text-base font-semibold text-gray-900 sm:order-2 sm:ml-8 sm:text-right"
                          >
                            $1259.00
                          </p>
                        </div>
                      </div>

                      <div
                        class="absolute top-0 right-0 flex sm:bottom-0 sm:top-auto"
                      >
                        <button
                          type="button"
                          class="flex rounded p-2 text-center text-gray-500 transition-all duration-200 ease-in-out focus:shadow hover:text-gray-900"
                        >
                          <svg
                            class="h-5 w-5"
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                          >
                            <path
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              stroke-width="2"
                              d="M6 18L18 6M6 6l12 12"
                              class=""
                            ></path>
                          </svg>
                        </button>
                      </div>
                    </div>
                  </li>
                  <li
                    class="flex flex-col space-y-3 py-6 text-left sm:flex-row sm:space-x-5 sm:space-y-0"
                  >
                    <div class="shrink-0 relative">
                      <span
                        class="absolute top-1 left-1 flex h-6 w-6 items-center justify-center rounded-full border bg-white text-sm font-medium text-gray-500 shadow sm:-top-2 sm:-right-2"
                        >1</span
                      >
                      <img
                        class="h-24 w-24 max-w-full rounded-lg object-cover"
                        src="https://tribratanews.polri.go.id/web/image/blog.post/50469/image"
                        alt=""
                      />
                    </div>

                    <div class="relative flex flex-1 flex-col justify-between">
                      <div class="sm:col-gap-5 sm:grid sm:grid-cols-2">
                        <div class="pr-8 sm:pr-5">
                          <p class="text-base font-semibold text-gray-900">
                            menu terbaik
                          </p>
                          <p class="mx-0 mt-1 mb-0 text-sm text-gray-400">
                            36EU - 4US
                          </p>
                        </div>

                        <div
                          class="mt-4 flex items-end justify-between sm:mt-0 sm:items-start sm:justify-end"
                        >
                          <p
                            class="shrink-0 w-20 text-base font-semibold text-gray-900 sm:order-2 sm:ml-8 sm:text-right"
                          >
                            $1259.00
                          </p>
                        </div>
                      </div>

                      <div
                        class="absolute top-0 right-0 flex sm:bottom-0 sm:top-auto"
                      >
                        <button
                          type="button"
                          class="flex rounded p-2 text-center text-gray-500 transition-all duration-200 ease-in-out focus:shadow hover:text-gray-900"
                        >
                          <svg
                            class="block h-5 w-5"
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                          >
                            <path
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              stroke-width="2"
                              d="M6 18L18 6M6 6l12 12"
                              class=""
                            ></path>
                          </svg>
                        </button>
                      </div>
                    </div>
                  </li>
                </ul>
              </div>

              <!-- <hr class="mx-0 mt-6 mb-0 h-0 border-r-0 border-b-0 border-l-0 border-t border-solid border-gray-300" /> -->

              <div class="mt-6 space-y-3 border-t border-b py-8">
                <div class="flex items-center justify-between">
                  <p class="text-gray-400">Subtotal</p>
                  <p class="text-lg font-semibold text-gray-900">$2399.00</p>
                </div>
                <div class="flex items-center justify-between">
                  <p class="text-gray-400">Shipping</p>
                  <p class="text-lg font-semibold text-gray-900">$8.00</p>
                </div>
              </div>
              <div class="mt-6 flex items-center justify-between">
                <p class="text-sm font-medium text-gray-900">Total</p>
                <p class="text-2xl font-semibold text-gray-900">
                  <span class="text-xs font-normal text-gray-400">USD</span>
                  2499.00
                </p>
              </div>

              <div class="mt-6 text-center">
                <button
                  type="button"
                  class="group inline-flex w-full items-center justify-center rounded-md bg-gray-800 px-6 py-4 text-lg font-semibold text-white transition-all duration-200 ease-in-out focus:shadow hover:bg-pink-500"
                >
                  Place Order
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="group-hover:ml-8 ml-4 h-6 w-6 transition-all"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M13 7l5 5m0 0l-5 5m5-5H6"
                    />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
