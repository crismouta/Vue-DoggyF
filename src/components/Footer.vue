<template>
  <div class="footercontainer ">
    <div class="d-flex flex-row p-2">
      <b-icon icon="instagram" class="p-4" aria-hidden="true" variant="dark" style="cursor: pointer;"></b-icon>
      <b-icon icon="facebook" class="p-4" aria-hidden="true"  variant="dark" style="cursor: pointer;"></b-icon>
      <b-icon icon="linkedin" class="p-4" aria-hidden="true"  variant="dark" style="cursor: pointer;"></b-icon>
    </div>
    <div >
      <p class="pb-2">Developed by MuyDiversos</p>
    </div>
  </div>
</template>

<script>

export default {
name: "Footer",

};

</script>

<style>
.footercontainer {
  height: 110px;
  width: 100%;
  background: #e07a1b;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  bottom:0;
  
  
}
</style>
