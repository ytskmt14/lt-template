<template>
  <div class="container mx-auto mt-3 px-8">
    <div class="mb-8">
        <slot/>
    </div>
    <div class="grid grid-cols-2">
      <div>
        <slot name="left_column"/>
      </div>
      <div>
        <slot name="right_column"/>
      </div>
    </div>

  </div>
</template>
