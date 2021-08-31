<template>
  <div class="bg-white md:hidden mt-12 py-5 mx-5 rounded-2xl">
      <!-- Buttons -->
      <div id="buttons" class="flex justify-evenly gap-8">
          <button class="inline-block mt-4 border border-purple-800 rounded-2xl px-5 py-1">Sign up</button>
          <button class="inline-block mt-4 bg-purple-900 text-white border border-purple-800 rounded-2xl px-7 py-1">Login</button>
      </div>
      <!-- Genders -->
      <div id="gender-card" class="flex justify-evenly mt-3">
          <div id="gender-male">
              <img src="../assets/images/CardMale.svg" alt="male-card">
          </div>
          <div id="gender-female">
              <img src="../assets/images/CardFemale.svg" alt="female-card">
          </div>
      </div>
      <!-- Forms -->
      <div id="form-control" class="flex justify-center mt-6">
          <form>
            <div id="inputs">
                <div id="search-bar" class="relative">
                  <div class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none">
                    <i class=" far fa-user mr-3 mb-6 text-gray-300"></i>
                  </div>
                    <input type="text" class="px-12 py-2.5 border border-purple-600 rounded-3xl inline-block mb-5 focus:outline-none" placeholder="Username"/>
                </div>
                <div id="search-bar" class="relative">
                   <div class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none">
                       <i class=" far fa-user mr-3 mb-6 text-gray-300"></i>
                   </div>
                      <input type="text" class="px-12 py-2.5 border border-purple-600 rounded-3xl inline-block mb-5 focus:outline-none" placeholder="Mail"/>
                </div>
                <div id="search-bar" class="relative">
                <div class="absolute inset-y-0 right-0 flex items-center px-2 pointer-events-none">
                    <i class="fas fa-chevron-down mr-3 mb-5 text-gray-300"></i>
                </div>
                    <input type="select" class="px-12 py-2.5 border border-purple-600 rounded-3xl inline-block mb-5 focus:outline-none" placeholder="What Are Your Interests?"/>
                </div>
            </div>
          </form>
      </div>
      <!-- Plus Icon -->
      <div class="flex justify-center my-3">
          <figure>
              <img src="../assets/images/plusicon.svg" alt="plus-icon">
          </figure>
      </div>
  </div>
</template>

<script>
export default {}
</script>
<style></style>