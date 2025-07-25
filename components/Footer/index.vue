<template>
  <footer>
    <PageContainer class="flex flex-col">
      <div class="py-20 flex justify-between items-center">
        <img src="/images/brands/ricky-and-morty-logo.png" />

        <BackToTop />
      </div>

      <div class="border-t-2 flex justify-between py-6">
        <p>&copy; {{ new Date().getFullYear() }}</p>

        <span class="flex items-center gap-2">
          <IconsCode />

          <p>
            Desenvolvido por
            <span class="text-[#11B0C8] font-bold">Código ao Ponto</span>
          </p>
        </span>
      </div>
    </PageContainer>
  </footer>
</template>
