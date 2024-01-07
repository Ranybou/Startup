<template>
  <div class="min-h-screen bg-green-400">
    <div class="container mx-auto px-3 flex flex-wrap items-center justify-center text-center py-5">
   
      <Nav></Nav>
      <BackToTopButton/>
      <slot></slot>
    </div>
  </div>
</template>
