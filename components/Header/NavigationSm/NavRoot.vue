<template>
  <div>
    <div class="header-block">
      <div class="location-selector-box">
        <PaperPlaneIcon />
        <LocationSelector />
      </div>
      <div>Войти</div>
    </div>
    <ul>
      <li>
        <div>
          <SearchIcon />
          <SearchField class="search-box" />
        </div>
      </li>
      <li>
        <a href="/">New</a>
      </li>
      <li>
        <div @click="$store.commit('changeSmMenuPage', 'catalog')">
          <span> Каталог </span>
          <Arrow class="arrow" />
        </div>
      </li>
      <li>
        <a href="/"> Скоро</a>
      </li>
      <li>
        <a href="/"> Скидки</a>
      </li>
      <li>
        <a href="/"> Lookbook</a>
      </li>
      <li>
        <a href="/"> Сертификаты</a>
      </li>
      <li>
        <a href="/"> О Нас</a>
      </li>
      <li>
        <a href="/"> Instastore</a>
      </li>
      <li>
        <a href="/"> Вакансии</a>
      </li>
      <li>
        <a href="/"> Мы в Instagram</a>
      </li>
      <li>
        <div @click="$store.commit('changeSmMenuPage', 'buyersInfo')">
          <span> Покупателям</span>
          <Arrow class="arrow" />
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import LocationSelector from '@/components/UI/LocationSelector'
import SearchIcon from '@/components/UI/IconsSvg/SearchIcon'
import PaperPlaneIcon from '@/components/UI/IconsSvg/PaperPlaneIcon'
import SearchField from '@/components/UI/SearchField'
import Arrow from '@/components/UI/IconsSvg/Arrow.vue'

export default {
  components: {
    LocationSelector,
    SearchIcon,
    PaperPlaneIcon,
    SearchField,
    Arrow,
  },
}
</script>

<style scoped>
.location-selector-box {
  display: flex;
  column-gap: 10px;
}

.search-box {
  margin-left: 15px;
}
.arrow {
  transform: rotate(-180deg);
  position: absolute;
  right: 10%;
}
</style>
