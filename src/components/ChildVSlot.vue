<template>
<div>
  <h4 class="weirdRainbow">
    <p>Incredibly important information..</p>
  <slot/> <!-- slot outlet => this is where the vslot will output. anything above or below this will show in relation to <slot/ > -->
	</h4>
</div>
</template>

<style>
.weirdRainbow {
  color: black;
  background: linear-gradient(315deg, #d38342 25%, #64ff7e);
  border: none;
  padding: 5px 10px;
  margin: 5px;
  border-radius: 8px;

}
</style>