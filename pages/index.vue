
<template >
  <div>
    <div></div>
    <div class="max-w-sm rounded overflow-hidden shadow-lg mb-4 dark:bg-gray-900"></div>
    <nav>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <div class="flex items-center">
            <!-- LOGO as Text -->
            <div class="flex-shrink-0">
              <p class="headerLogo">Tjark Ziehm</p>
            </div>
            <!--   -->
            <div class="hidden md:block">
              <div class="ml-10 flex items-baseline">
                <a href="#"
                  class="px-3 py-2 rounded-md text-sm font-medium text-white bg-gray-900 focus:outline-none focus:text-white focus:bg-gray-700">Mainpage</a>
                <a href="#"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Quantum</a>
                <a href="#"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">MindSet</a>
                <a href="#"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Talks</a>
                <a href="#"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Tweets</a>
              </div>
            </div>

          </div>

          <div class="hidden md:block">
            <div class="ml-4 flex items-center md:ml-6">


              <!-- Environment dropdown -->
              <div class="ml-3 relative">

                <div>
                  <button @click="toggle"
                    class="max-w-xs flex items-center text-sm rounded-full text-white focus:outline-none focus:shadow-solid"
                    id="user-menu" aria-label="User menu" aria-haspopup="true">
                    <p>Environment</p>
                  </button>
                </div>

                <transition enter-active-class="transition ease-out duration-100"
                  enter-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100"
                  leave-active-class="transition ease-in duration-75" leave-class="transform opacity-100 scale-100"
                  leave-to-class="transform opacity-0 scale-95">
                  <div v-show="isOpen" class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg">
                    <div class="py-1 rounded-md bg-white shadow-xs" role="menu" aria-orientation="vertical"
                      aria-labelledby="user-menu">
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100" role="menuitem">Your
                        Profile</a>
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                        role="menuitem">Settings</a>
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100" role="menuitem">Sign
                        out</a>
                    </div>
                  </div>
                </transition>
              </div>

              <!-- Social dropdown -->
              <div class="ml-3 relative">

                <div>
                  <button @click="toggle"
                    class="max-w-xs flex items-center text-sm rounded-full text-white focus:outline-none focus:shadow-solid"
                    id="user-menu" aria-label="User menu" aria-haspopup="true">
                    <p>Social</p>
                  </button>
                </div>

                <transition enter-active-class="transition ease-out duration-100"
                  enter-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100"
                  leave-active-class="transition ease-in duration-75" leave-class="transform opacity-100 scale-100"
                  leave-to-class="transform opacity-0 scale-95">
                  <div v-show="isOpen" class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg">
                    <div class="py-1 rounded-md bg-white shadow-xs" role="menu" aria-orientation="vertical"
                      aria-labelledby="user-menu">
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100" role="menuitem">Your
                        Profile</a>
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                        role="menuitem">Settings</a>
                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100" role="menuitem">Sign
                        out</a>
                    </div>
                  </div>
                </transition>
              </div>

            </div>
          </div>

          <div class="-mr-2 flex md:hidden">
            <!-- Mobile menu button -->
            <button @click="toggle"
              class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:bg-gray-700 focus:text-white">
              <svg :class="[isOpen ? 'hidden' : 'block', 'h-6 w-6']" stroke="currentColor" fill="none"
                viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16">
                </path>
              </svg>
              <svg :class="[isOpen ? 'block' : 'hidden', 'h-6 w-6']" stroke="currentColor" fill="none"
                viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
              </svg>
            </button>
          </div>

        </div>
      </div>

      <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
        <div class="px-2 pt-2 pb-3 sm:px-3">
          <a href="#"
            class="block px-3 py-2 rounded-md text-base font-medium text-white bg-gray-900 focus:outline-none focus:text-white focus:bg-gray-700">MainPage</a>
          <a href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Quantum</a>
          <a href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Social</a>
          <a href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Environment</a>
          <a href="#"
            class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Tweets</a>
        </div>

        <div class="pt-4 pb-3 border-t border-gray-700">
          <div class="flex items-center px-5">
            <div class="flex-shrink-0">
              <img class="h-10 w-10 rounded-full"
                src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                alt>
            </div>

            <div class="ml-3">
              <div class="text-base font-medium leading-none text-white">Tjark Ziehm</div>
              <div class="mt-1 text-sm font-medium leading-none text-gray-400">tjark.ziehm@ohioh.de</div>
            </div>

          </div>
          <div class="mt-3 px-2">
            <a href="#"
              class="block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Your
              Profile</a>
            <a href="#"
              class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Settings</a>
            <a href="#"
              class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Sign
              out</a>
          </div>
        </div>
      </div>
    </nav>

    <!-- Header -->
    <header class="bg-white shadow">
      <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
        <h1 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">MainPage</h1>
      </div>
    </header>

    <main>
      <div class="grid">
        <!-- First Views -->

        <div
          class="max-w-2xl mx-auto py-24 px-4 grid items-center grid-cols-1 gap-y-16 gap-x-8 sm:px-6 sm:py-32 lg:max-w-7xl lg:px-8 lg:grid-cols-2">
          <div>
            <h2 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">Let' rock ...</h2>
            <!--
              <p class="mt-4 text-gray-500">The walnut wood card tray is precision milled to perfectly fit a stack of
                Focus cards. The powder coated steel divider separates active cards from new ones, or can be used to
                archive important task lists.</p>
              -->

            <dl class="mt-16 grid grid-cols-2 gap-x-6 gap-y-10 sm:grid-cols-2 sm:gap-y-16 lg:gap-x-8">

              <div class="border-t border-gray-200 pt-4">
                <dt class="font-medium text-gray-900">ThinkTank</dt>
                <dd class="mt-2 text-sm text-gray-500">more ...</dd>
              </div>

              <div class="border-t border-gray-200 pt-4">
                <dt class="font-medium text-gray-900">Visioner</dt>
                <dd class="mt-2 text-sm text-gray-500">more ...</dd>
              </div>

              <div class="border-t border-gray-200 pt-4">
                <dt class="font-medium text-gray-900">Enterpreneur</dt>
                <dd class="mt-2 text-sm text-gray-500">more ...</dd>
              </div>




            </dl>

            <div class="font-medium text-gray-900">
              <img src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-01.jpg"
                alt="Walnut card tray with white powder coated steel divider and 3 punchout holes."
                class="bg-gray-100 rounded-lg">
            </div>


          </div>

        </div>

        <!-- Section: Themes
            <div
              class="max-w-2xl mx-auto py-24 px-4 grid items-center grid-cols-1 gap-y-16 gap-x-8 sm:px-6 sm:py-32 lg:max-w-7xl lg:px-8 lg:grid-cols-2">
              <div>
                <h2 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">Technical Specifications
                </h2>
                <p class="mt-4 text-gray-500">The walnut wood card tray is precision milled to perfectly fit a stack of
                  Focus cards. The powder coated steel divider separates active cards from new ones, or can be used to
                  archive important task lists.</p>

                <dl class="mt-16 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 sm:gap-y-16 lg:gap-x-8">
                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Origin</dt>
                    <dd class="mt-2 text-sm text-gray-500">Designed by Good Goods, Inc.</dd>
                  </div>

                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Material</dt>
                    <dd class="mt-2 text-sm text-gray-500">Solid walnut base with rare earth magnets and powder coated
                      steel card cover</dd>
                  </div>

                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Dimensions</dt>
                    <dd class="mt-2 text-sm text-gray-500">6.25&quot; x 3.55&quot; x 1.15&quot;</dd>
                  </div>

                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Finish</dt>
                    <dd class="mt-2 text-sm text-gray-500">Hand sanded and finished with natural oil</dd>
                  </div>

                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Includes</dt>
                    <dd class="mt-2 text-sm text-gray-500">Wood card tray and 3 refill packs</dd>
                  </div>

                  <div class="border-t border-gray-200 pt-4">
                    <dt class="font-medium text-gray-900">Considerations</dt>
                    <dd class="mt-2 text-sm text-gray-500">Made from natural materials. Grain and color vary with each
                      item.</dd>
                  </div>
                </dl>
              </div>
              <div class="grid grid-cols-2 grid-rows-2 gap-4 sm:gap-6 lg:gap-8">
                <img src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-01.jpg"
                  alt="Walnut card tray with white powder coated steel divider and 3 punchout holes."
                  class="bg-gray-100 rounded-lg">
                <img src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-02.jpg"
                  alt="Top down view of walnut card tray with embedded magnets and card groove."
                  class="bg-gray-100 rounded-lg">
                <img src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-03.jpg"
                  alt="Side of walnut card tray with card groove and recessed card area."
                  class="bg-gray-100 rounded-lg">
                <img src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-04.jpg"
                  alt="Walnut card tray filled with cards and card angled in dedicated groove."
                  class="bg-gray-100 rounded-lg">
              </div>
            </div>
            -->
        <!-- /End replace -->
      </div>
    </main>

    <div class="flex">
      <div class="box1 flex-none hover:flex-1">
        <p>Black</p>
      </div>
      <div class="box2 flex-none hover:flex-1">
        <p>Green</p>
      </div>
      <div class="box3 grow-1 w-32  hover:flex-1">
        <p>Gray</p>
      </div>
    </div>

    <div>
      <p>Space 1</p>
    </div>

    <div class="flex h-32">
      <div class="box1 flex-none hover:flex-1">
        <p>Black</p>
      </div>
      <div class="box2 flex-none hover:flex-1">
        <p>Green</p>
      </div>
      <div class="box3 flex-auto hover:flex-1">
        <p>Gray</p>
      </div>
    </div>

    <div>
      <p>Space 2</p>
    </div>

    <div class="flex h-32">
      <div class="box1 grow h-14 hover:flex-1 ...">
        <p>Black</p>
      </div>
      <div class="box2 grow-0 h-14 hover:flex-1 ...">
        <p>Green</p>
      </div>
      <div class="box3 grow h-14 hover:flex-1 ...">
        <p>Gray</p>
      </div>
    </div>

    <div>
      <p>Space 3</p>
    </div>

    <div class="flex h-32">
      <div class="box1 grow-[1] ...">
        <p>Black</p>
      </div>
      <div class="box2 grow-[2] ...">
        <p>Green</p>
      </div>
      <div class="box3 grow-[3] ...">
        <p>Gray</p>
      </div>
    </div>

    <div>
      <p>Space 4</p>
    </div>

    <div class="flex h-10 justify-between">
      <div class="box1 grow-[1] hover:grow-[4] ...">
        <p>Black</p>
      </div>
      <div class="box2 grow-[2] hover:grow-[4] ...">
        <p>Green</p>
      </div>
      <div class="box3 shrink-1 hover:grow-[4] ...">
        <p>Gray</p>
      </div>
    </div>

    <div>
      <p>Space 5</p>
    </div>

    <div class="flex justify-between flex-nowrap ...">
      <div class="box1 order-first hover:order-last">01</div>
      <div class="box2 order-last">02</div>
      <div class="box3">03</div>
    </div>

    <div>
      <p>Space 6</p>
    </div>

    <div class="flex justify-between flex-col  ...">
      <div class="box1 ">01</div>
      <div class="box2 order-last">02</div>
      <div class="box3">03</div>
    </div>



  </div>
  
</template>

<style >
.box1 {
  background-color: black;
  color: white;
  font-size: 10;

}

.box2 {
  background-color: green;
  color: black;
  font-size: 10;
}

.box3 {
  background-color: gray;
  color: black;
  font-size: 10;
}

.headerLogo {
  color: white;
  font-size: 5rem;
  font-family: Roboto;
  padding: 2rem;
}

.test {
  color: rgb(39, 27, 167);
}

.working {
  color: rgb(27, 167, 29);
}

.gray {
  color: rgb(167, 27, 62);
}
</style>





