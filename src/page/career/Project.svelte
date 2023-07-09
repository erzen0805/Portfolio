<script>
  export let name;
  export let imgSrc;
</script>

<div class="root">
  <h3 class="name">{name}</h3>
  <div style="text-align: center;">
    <img src={imgSrc} style="border-radius: 10px; max-height: 300px;" alt={name}/>
  </div>
  <slot />
</div>

<style>
.root {
  padding: 20px 20px 40px 20px;
  font-family: KoHo;
  font-size: 1.25rem;
  font-weight: 700;
  color: rgb(146, 146, 146);
}
.name {
  font-size: 1.8rem;
  font-weight: 700;
  margin-bottom: 15px;
  display: flex;
  flex-direction: column;
  color: rgb(184, 232, 41);
}
</style>