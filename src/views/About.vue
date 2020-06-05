<template>
  <section class="block">
      <h2 class="block__title">{{title}}</h2>
      <div class="block__info">
          <p class="block__name">{{name}}</p>
          <div class="block__links">
              <a href="tel:+79259049590" class="block__link"><img src="" alt="" class="block__icon">Call me</a>
              <a href="https://wa.me/79259049590" class="block__link"><img src="" alt="" class="block__icon">Text me</a>
              <a href="mailto:alex.rodionov.xxxx@gmail.com" class="block__link"><img src="" alt="" class="block__icon">Write me</a>
          </div>
          <div class="block__todos">
              <p class="block__todo">Использовать одну из последних версий VUE <span class="done">done</span></p>
              <p class="block__todo">Можно использовать CLI <span class="done">done</span></p>
              <p class="block__todo">Отображает открытые задачи Github <span class="done">done</span></p>
              <p class="block__todo">Адаптивная и мобильная верстка <span class="done">done</span></p>
              <p class="block__todo">Простой читаемый код <span class="done">done</span></p>
              <p class="block__todo">Использовать Git <span class="done">done</span></p>
              <p class="block__todo">Не использовать css библиотеки <span class="done">done</span></p>
              <p class="block__todo">Стили изолированы <span class="done">done</span></p>
              <p class="block__todo">Scss <span class="done">done</span></p>
              <p class="block__todo">Индикация загрузки <span class="done">done</span></p>
              <p class="block__todo">Router <span class="done">done</span></p>
              <p class="block__todo">Few hover and active effects <span class="done">done</span></p>
              <p class="block__todo">Github pages для публикации <span class="done">done</span></p>
          </div>
      </div>




  </section>
</template>

<script>

export default {
  data () {
    return {
        title : 'Author remarks:',
        name: 'Alexander Rodionov',

    }
  },




}
</script>


<style scoped lang="scss">
$color-1: #3C3C3C;
.done{
    color: #6bba6c;
}
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
    &__info {
        width: 500px;
        padding: 20px;
        border: 1px solid #e4e4e4;
        border-radius: 2px;
    }
    &__name {
        font-family: sans-serif;
        font-style: italic;
        font-size: 26px;
        color: #7e7e7e;
        font-weight: bold;
        margin-bottom: 20px;

    }
    &__links {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        margin-bottom: 40px;
    }
    &__link {
        font-family: sans-serif;
        font-size: 14px;
        color: grey;

        text-decoration: none;
        cursor: pointer;
        margin-right: 20px;
        &:hover {
            color: $color-1;
        }

    }
    .todos {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;

    }
    &__todo {
        font-family: sans-serif;
        font-size: 16px;
        font-weight: 300;
        line-height: 1.2;
        color: $color-1;
        margin-bottom: 10px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;



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
        &__info {
            width: 500px;
            padding: 20px;
            border: 1px solid #e4e4e4;
            border-radius: 2px;
        }
        &__name {
            font-family: sans-serif;
            font-style: italic;
            font-size: 26px;
            color: #7e7e7e;
            font-weight: bold;
            margin-bottom: 20px;

        }
        &__links {
            width: 100%;
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: flex-start;
            margin-bottom: 40px;
        }
        &__link {
            font-family: sans-serif;
            font-size: 14px;
            color: grey;

            text-decoration: none;
            cursor: pointer;
            margin-right: 20px;
            &:hover {
                color: $color-1;
            }

        }
        .todos {
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: flex-start;

        }
        &__todo {
            font-family: sans-serif;
            font-size: 16px;
            font-weight: 300;
            line-height: 1.2;
            color: $color-1;
            margin-bottom: 10px;
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;



        }

    }
}



/* SCREEN (min-width: 601px) and (max-width: 900px) =============== */
@media all and (min-width: 601px) and (max-width: 900px)  {


        .block {
            display: flex;
            width: 90%;
            max-width: 700px;
            min-width: 500px;
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
            &__info {
                width: 400px;
                padding: 20px;
                border: 1px solid #e4e4e4;
                border-radius: 2px;
            }
            &__name {
                font-family: sans-serif;
                font-style: italic;
                font-size: 26px;
                color: #7e7e7e;
                font-weight: bold;
                margin-bottom: 20px;

            }
            &__links {
                width: 100%;
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: flex-start;
                margin-bottom: 40px;
            }
            &__link {
                font-family: sans-serif;
                font-size: 14px;
                color: grey;

                text-decoration: none;
                cursor: pointer;
                margin-right: 20px;
                &:hover {
                    color: $color-1;
                }

            }
            .todos {
                width: 100%;
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                justify-content: flex-start;

            }
            &__todo {
                font-family: sans-serif;
                font-size: 16px;
                font-weight: 300;
                line-height: 1.2;
                color: $color-1;
                margin-bottom: 10px;
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: space-between;



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
                    font-size: 40px;
                    color: $color-1;
                    font-weight: bold;
                    margin-bottom: 40px;


                }
                &__info {
                    width: 350px;
                    padding: 10px;
                    border: 1px solid #e4e4e4;
                    border-radius: 2px;
                }
                &__name {
                    font-family: sans-serif;
                    font-style: italic;
                    font-size: 20px;
                    color: #7e7e7e;
                    font-weight: bold;
                    margin-bottom: 20px;

                }
                &__links {
                    width: 100%;
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: flex-start;
                    margin-bottom: 40px;
                }
                &__link {
                    font-family: sans-serif;
                    font-size: 14px;
                    color: grey;

                    text-decoration: none;
                    cursor: pointer;
                    margin-right: 20px;
                    &:hover {
                        color: $color-1;
                    }

                }
                .todos {
                    width: 100%;
                    display: flex;
                    flex-direction: column;
                    align-items: flex-start;
                    justify-content: flex-start;

                }
                &__todo {
                    font-family: sans-serif;
                    font-size: 14px;
                    font-weight: 300;
                    line-height: 1.2;
                    color: $color-1;
                    margin-bottom: 10px;
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: space-between;



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
                    margin-top: 20px;
                    margin-bottom: 40px;
                    &__title {
                        font-family: sans-serif;
                        font-size: 30px;
                        color: $color-1;
                        font-weight: bold;
                        margin-bottom: 20px;


                    }
                    &__info {
                        width: 90%;
                        padding: 10px;
                        border: 1px solid #e4e4e4;
                        border-radius: 2px;
                    }
                    &__name {
                        font-family: sans-serif;
                        font-style: italic;
                        font-size: 20px;
                        color: #7e7e7e;
                        font-weight: bold;
                        margin-bottom: 20px;

                    }
                    &__links {
                        width: 100%;
                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        justify-content: flex-start;
                        margin-bottom: 40px;
                    }
                    &__link {
                        font-family: sans-serif;
                        font-size: 14px;
                        color: grey;

                        text-decoration: none;
                        cursor: pointer;
                        margin-right: 20px;
                        &:hover {
                            color: $color-1;
                        }

                    }
                    .todos {
                        width: 100%;
                        display: flex;
                        flex-direction: column;
                        align-items: flex-start;
                        justify-content: flex-start;

                    }
                    &__todo {
                        font-family: sans-serif;
                        font-size: 14px;
                        font-weight: 300;
                        line-height: 1.2;
                        color: $color-1;
                        margin-bottom: 10px;
                        display: flex;
                        flex-direction: row;
                        align-items: center;
                        justify-content: space-between;



                    }

                }




}






</style>
