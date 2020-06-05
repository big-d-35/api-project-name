<template>
  <main id="app">
    <div id="nav" class="navigation">
      <router-link to="/"
      class="navigation__link"
      active-class='navigation__link-active'
      exact
      >Github issue</router-link> |

      <router-link to="/about"
      class="navigation__link"
      active-class='navigation__link-active'
      exact
      >About</router-link>
    </div>
    <router-view/>
    <vue-progress-bar></vue-progress-bar>
</main>
</template>

<style scoped lang="scss">
@import './assets/css/reset.min.css';
$color-1: #3C3C3C;
#app {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}

.navigation {
    margin-top: 40px;
    margin-bottom: 20px;
    &__link {
        font-size: 20px;
        text-decoration: none;
        color: #aaaaaa;
        cursor: pointer;
        &-active {
            color: $color-1;
        }
        &:hover {
            color: $color-1;
        }

    }

}
</style>
