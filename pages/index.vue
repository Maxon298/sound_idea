<template>
  <div class="home-page">
    <div class="_container">
      <div class="home-page__intro">
      <div class="home-page__content">
        <img width=770 height=109 src="@/assets/img/banner.jpg" alt="Music Fest" class="banner">
        <div class="home-page__inner">
          <div class="home-page__column">
            <h3 class="home-page__column_title">Last Acapellas</h3>
              <Player
                v-for="player in acapellas_list"
                    :key="`player-${player.id}`"
                    :title="player.title"
                    :date="player.date"
                    :like_count="player.like_count"
                    :music="player.music"
                    :author="player.author"
                    :genre="player.type"
                    :tags="player.tags"
                />
          </div>
          <div class="home-page__column">
            <h3 class="home-page__column_title">Last Loops</h3>
            <Player
              v-for="player in loops_list"
              :key="`player-${player.id}`"
              :title="player.title"
              :date="player.date"
              :like_count="player.like_count"
              :music="player.music"
              :author="player.author"
              :genre="player.type"
              :tags="player.tags"
            />
          </div>
      </div>

      </div>
      <div class="home-page__sidebar">
        <Search/>
      </div>
      </div>
    </div>
    </div>

</template>

<script>
export default {
  data: () => ({
        acapellas_list: [
            {
                id: 1,
                title: '1',
                date: new Date(),
                like_count: 60,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rock',
                tags: [
                    'rap',
                    'rock',
                    'alt'
                ]
            },
            {
                id: 2,
                title: '2',
                date: new Date(),
                like_count: 33,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rock',
                tags: [
                    '1',
                    '2',
                    '3'
                ]
            },
            {
                id: 3,
                title: '3',
                date: new Date(),
                like_count: 0,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rap',
                tags: [
                    '1',
                    '2',
                    '3'
                ]
            }
        ],
        loops_list: [
            {
                id: 1,
                title: '1',
                date: new Date(),
                like_count: 60,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rock',
                tags: [
                    'rap',
                    'rock',
                    'alt'
                ]
            },
            {
                id: 2,
                title: '2',
                date: new Date(),
                like_count: 33,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rock',
                tags: [
                    '1',
                    '2',
                    '3'
                ]
            },
            {
                id: 3,
                title: '3',
                date: new Date(),
                like_count: 0,
                music: null,
                author: {
                    id: 1,
                    first_name: 'James',
                    last_name: 'Arthur',
                },
                type: 'Rap',
                tags: [
                    '1',
                    '2',
                    '3'
                ]
            }
        ],
        news: [
          {
            album_cover: null,
            date: new Date(),
            title: 'ASKING ALEXANDRIA NEW ALBUM “ANTISOCIALIST”',
            description: 'Asking Alexandria are announcing their sixth full-length record will be titled Like A House On Fire three years on from their self-titled 2017 album.'
          }
        ]
    }),

  components: {
    Player: () => import(`@/components/player.vue`),
    Search: () => import(`@/components/search.vue`)
  }
}
</script>

<style lang="scss">
  .home-page{
    margin-top: 38px;
  }

  .home-page__intro{
    display: flex;
  }

  .home-page__content{
    width: 80%;
    min-width: 770px;
  }

  .home-page__inner{
    display: flex;
  }

  .home-page__column{
    display: grid;
    margin-right: 30px;
    grid-template-columns: repeat(1, 1fr);
    grid-gap: 20px;
  }

  .home-page__column_title{
    text-align: center;
    font-weight: 700;
    font-size: 15px;
    line-height: 18px;
    color: #000000;
  }

  .home-page__sidebar{
    width: 20%;
    min-width: 370px;
  }

</style>
