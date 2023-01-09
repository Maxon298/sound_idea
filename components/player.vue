<template>
  <div class="player">
    <div class="player_inner">
      <div class="player_header">
        <h4 class="player_title">
          {{title}}
        </h4>
        <p class="player_date">26.11.2022</p>
      </div>
      <div class="player_controls">
        <div class="player_timescale">
          <div class="player_timescale_button">
            <img class="player_timescale_button-img" width='39.94' height='34' src="@/assets/img/svg/play-button.svg" alt="Play" >
          </div>
          <img src="@/assets/img/music-line.png" width="175.5" height="18" class="player_timescale_audio">
        </div>
        <div class="player_like">
          <img src="@/assets/img/svg/player-like.svg" alt="Like" class="player_like_like-img">
          <p class="player_like_like-count">{{like_count}}</p>
        </div>
      </div>
      <div class="player_footer">
        <div class="player_author">
          <img src="@/assets/img/svg/author-icon.svg" alt="Author Icon" class="player_author_img">
          <p class="player_author_name">{{author.first_name}} {{author.last_name}}</p>
          <div class="player_author_genre">
             <p class="player_author_genre_name">{{genre}}</p>
          </div>
        </div>
         <div class="player_related-genres">
          <p
            class="player_related-genres_genre"
            v-for="(tag, index) in tags"
            :key="`tag-${index}`"
          >
            {{tag}}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "@/assets/css/player.scss"
import { title } from "process";

export default {
  name: "Player",
  props: [
    'title',
    'date',
    'like_count',
    'music',
    'author',
    'genre',
    'tags'
  ]
}
</script>
