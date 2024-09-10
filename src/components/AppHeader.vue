<script>
export default {
  data() {
    return {
      links:[
        {
          label: 'CHARACTERS',
          href: '#'
        },
        {
          label: 'COMICS',
          href: '#'
        },
        {
          label: 'MOVIES',
          href: '#'
        },
        {
          label: 'TV',
          href: '#'
        },
        {
          label: 'GAMES',
          href: '#'
        },
        {
          label: 'COLLECTIBLES',
          href: '#'
        },
        {
          label: 'VIDEOS',
          href: '#'
        },
        {
          label: 'FANS',
          href: '#'
        },
        {
          label: 'NEWS',
          href: '#'
        },
        {
          label: 'SHOP',
          href: '#'
        }
      ],
    }
  }
}
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-2 py-2">
          <img src="/img/dc-logo.png" alt="DC_Logo">
        </div>
        <div class="col-10 py-2">
          <ul class="nav justify-content-end h-100 align-items-center">
            <li class="nav-item" v-for="link, index in links" :key="index">
              <a class="nav-link" :href="link.href">{{ link.label }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header{
    
    .container{
      .row{
        div.col-2{
          img{
            width:80px;
          }
        }
        div.col-10{
        ul{
          li{
            a{
              color:#1C1C1C;
              font-weight:bold;
            }
          }
        }
      }
    }
    }
  }
</style>
