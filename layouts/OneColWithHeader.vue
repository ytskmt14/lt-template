<template>
  <div class="container mx-auto mt-3 px-8">
    <div class="mb-8">
        <slot/>
    </div>
    <div class="grid grid-cols-1">
      <div>
        <slot name="content"/>
      </div>
    </div>

  </div>
</template>
