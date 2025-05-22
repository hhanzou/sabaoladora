<template>
  <UApp class="bg-pink-50 min-h-screen">
    <!-- Navbar full width -->
    <nav class="w-full py-4 border-b bg-pink-200 border-pink-900 mb-6">
      <UContainer class="flex items-center justify-between">
        <div class="flex items-center gap-2 text-xl font-bold text-pink-600">
          <img src="/soap-logo.png" alt="logo" class="w-20 h-20" />
          Sabãoladora
        </div>
      </UContainer>
    </nav>

    <!-- Page content -->
    <UContainer>
      <NuxtPage />
    </UContainer>
  </UApp>
</template>
