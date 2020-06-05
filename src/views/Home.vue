<template>
  <section class="block">
      <h1 class="block__title">{{title}}</h1>
      <div class="issues">
          <div class="issues__block" v-for="post in posts" v-bind:key="post.id">
              <div class="issues__titles">
                  <img class="issues__img" :src="post.user.avatar_url" alt="authors image">
                  <h2 class="issues__title">{{post.title}}</h2>

              </div>

              <div class="issues__infos">
                  <p class="issues__info">ID:{{post.id}}</p>
                  <p class="issues__info">created: {{post.created_at}}</p>
                  <p class="issues__info">№ {{post.number}}</p>
                  <p class="issues__info">comments {{post.comments}}</p>
                  <a class="issues__link" :href="post.html_url" target="_blank">see at github</a>
              </div>


          </div>

      </div>

  </section>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
    title : 'Github vue issues:',
      posts: null,
      endpoint: 'https://api.github.com/repos/vuejs/vue/issues?q=is%3Aopen',
    }
  },

  created() {
    this.getAllPosts();
  },

  methods: {
    getAllPosts() {
      this.$Progress.start();
      axios.get(this.endpoint)
        .then(response => {
          this.posts = response.data;
          this.$Progress.finish()
          
        })
        .catch(error => {
          console.log('-----error-------');
          console.log(error);
          this.$Progress.fail();
        })
    }
  }
}
</script>

<style scoped lang="scss">
$color-1: #3C3C3C;
/* SCREEN (min-width: 1201px) =============== */
@media (min-width: 1201px) {

.block {
    display: flex;
    width: 100%;
    max-width: 1000px;
    min-width: 1000px;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    margin-top: 40px;
    margin-bottom: 40px;
    &__title {
        font-family: sans-serif;
        font-size: 40px;
        color: $color-1;
        font-weight: bold;
        margin-bottom: 40px;


    }

}

.issues {
    display: flex;
    flex-direction: column;;
    justify-content: flex-start;
    align-items: flex-start;
    width: 100%;
    &__block {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        border-bottom: 1px solid grey;


        margin-bottom: 30px;
    }
    &__titles {
        width: 100%;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        margin-bottom: 20px;
    }
    &__title {
        font-family: sans-serif;
        font-size: 18px;
        color: $color-1;
        font-weight: 400;
        text-transform: capitalize;

    }
    &__img {
        width: 60px;
        margin-right: 40px;
    }
    &__infos {
        width: 100%;

        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 10px;
    }
    &__info {
        font-family: sans-serif;
        font-size: 14px;
        color: grey;
        font-weight: 300;
        margin-right: 20px;
    }
    &__link {
        font-family: sans-serif;
        font-size: 14px;
        color: grey;
        font-weight: bold;
        text-decoration: none;
        cursor: pointer;
        &:hover {
            color: $color-1;
        }
    }
}

}



/* SCREEN (min-width: 901px) and (max-width: 1200px) =============== */
@media all and (min-width: 901px) and (max-width: 1200px)  {


    .block {
        display: flex;
        width: 90%;
        max-width: 1100px;
        min-width: 800px;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        margin-top: 40px;
        margin-bottom: 40px;
        &__title {
            font-family: sans-serif;
            font-size: 40px;
            color: $color-1;
            font-weight: bold;
            margin-bottom: 40px;


        }

    }

    .issues {
        display: flex;
        flex-direction: column;;
        justify-content: flex-start;
        align-items: flex-start;
        width: 100%;
        &__block {
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;
            border-bottom: 1px solid grey;


            margin-bottom: 30px;
        }
        &__titles {
            width: 100%;

            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: flex-start;
            margin-bottom: 20px;
        }
        &__title {
            font-family: sans-serif;
            font-size: 18px;
            color: $color-1;
            font-weight: 400;
            text-transform: capitalize;

        }
        &__img {
            width: 60px;
            margin-right: 40px;
        }
        &__infos {
            width: 100%;

            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        &__info {
            font-family: sans-serif;
            font-size: 14px;
            color: grey;
            font-weight: 300;
            margin-right: 20px;
        }
        &__link {
            font-family: sans-serif;
            font-size: 14px;
            color: grey;
            font-weight: bold;
            text-decoration: none;
            cursor: pointer;
            &:hover {
                color: $color-1;
            }
        }
    }



}



/* SCREEN (min-width: 601px) and (max-width: 900px) =============== */
@media all and (min-width: 601px) and (max-width: 900px)  {


        .block {
            display: flex;
            width: 90%;
            max-width: 800px;
            min-width: 500px;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            margin-top: 40px;
            margin-bottom: 40px;
            &__title {
                font-family: sans-serif;
                font-size: 30px;
                color: $color-1;
                font-weight: bold;
                margin-bottom: 40px;


            }

        }

        .issues {
            display: flex;
            flex-direction: column;;
            justify-content: flex-start;
            align-items: flex-start;
            width: 100%;
            &__block {
                width: 100%;
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                justify-content: flex-start;
                border-bottom: 1px solid grey;


                margin-bottom: 30px;
            }
            &__titles {
                width: 100%;

                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: flex-start;
                margin-bottom: 20px;
            }
            &__title {
                font-family: sans-serif;
                font-size: 18px;
                color: $color-1;
                font-weight: 400;
                text-transform: capitalize;

            }
            &__img {
                width: 50px;
                margin-right: 40px;
            }
            &__infos {
                width: 100%;

                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: space-between;
                margin-bottom: 10px;
            }
            &__info {
                font-family: sans-serif;
                font-size: 12px;
                color: grey;
                font-weight: 300;
                margin-right: 20px;
            }
            &__link {
                font-family: sans-serif;
                font-size: 14px;
                color: grey;
                font-weight: bold;
                text-decoration: none;
                cursor: pointer;
                &:hover {
                    color: $color-1;
                }
            }
        }




}


/* SCREEN (min-width: 401px) and (max-width: 600px) =============== */
@media all and (min-width: 401px) and (max-width: 600px)  {


            .block {
                display: flex;
                width: 90%;
                max-width: 500px;
                min-width: 300px;
                flex-direction: column;
                justify-content: flex-start;
                align-items: flex-start;
                margin-top: 40px;
                margin-bottom: 40px;
                &__title {
                    font-family: sans-serif;
                    font-size: 30px;
                    color: $color-1;
                    font-weight: bold;
                    margin-bottom: 40px;
                    line-height: 1.2;


                }

            }

            .issues {
                display: flex;
                flex-direction: column;;
                justify-content: flex-start;
                align-items: flex-start;
                width: 100%;
                &__block {
                    width: 100%;
                    display: flex;
                    flex-direction: column;
                    align-items: flex-start;
                    justify-content: flex-start;
                    border-bottom: 1px solid grey;


                    margin-bottom: 30px;
                }
                &__titles {
                    width: 100%;

                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: flex-start;
                    margin-bottom: 20px;
                }
                &__title {
                    font-family: sans-serif;
                    font-size: 18px;
                    color: $color-1;
                    font-weight: 400;
                    text-transform: capitalize;

                }
                &__img {
                    width: 60px;
                    margin-right: 20px;
                }
                &__infos {
                    width: 100%;

                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: space-between;
                    margin-bottom: 10px;
                }
                &__info {
                    font-family: sans-serif;
                    font-size: 10px;
                    color: grey;
                    font-weight: 300;
                    margin-right: 20px;
                }
                &__link {
                    font-family: sans-serif;
                    font-size: 14px;
                    color: grey;
                    font-weight: bold;
                    text-decoration: none;
                    cursor: pointer;
                    &:hover {
                        color: $color-1;
                    }
                }
            }






}



/* SCREEN (max-width: 400px) =============== */
@media all and (max-width: 400px)  {

                .block {
                    display: flex;
                    width: 90%;
                    max-width: 380px;
                    min-width: 300px;
                    flex-direction: column;
                    justify-content: flex-start;
                    align-items: flex-start;
                    margin-top: 40px;
                    margin-bottom: 40px;
                    &__title {
                        font-family: sans-serif;
                        font-size: 30px;
                        color: $color-1;
                        font-weight: bold;
                        margin-bottom: 40px;
                        line-height: 1.2;


                    }

                }

                .issues {
                    display: flex;
                    flex-direction: column;;
                    justify-content: flex-start;
                    align-items: flex-start;
                    width: 100%;
                    &__block {
                        width: 100%;
                        display: flex;
                        flex-direction: column;
                        align-items: flex-start;
                        justify-content: flex-start;
                        border-bottom: 1px solid grey;


                        margin-bottom: 30px;
                    }
                    &__titles {
                        width: 100%;

                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        justify-content: flex-start;
                        margin-bottom: 20px;
                    }
                    &__title {
                        font-family: sans-serif;
                        font-size: 18px;
                        color: $color-1;
                        font-weight: 400;
                        text-transform: capitalize;

                    }
                    &__img {
                        width: 60px;
                        margin-right: 20px;
                    }
                    &__infos {
                        width: 100%;

                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        justify-content: flex-end;
                        margin-bottom: 10px;
                    }
                    &__info {
                        display: none;
                        font-family: sans-serif;
                        font-size: 10px;
                        color: grey;
                        font-weight: 300;
                        margin-right: 20px;
                    }
                    &__link {
                        font-family: sans-serif;
                        font-size: 14px;
                        color: grey;
                        font-weight: bold;
                        text-decoration: none;
                        cursor: pointer;
                        &:hover {
                            color: $color-1;
                        }
                    }
                }







}






</style>
