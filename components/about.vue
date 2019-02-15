<template>
  <v-container grid-list-sm>
    <v-layout align-center justify-center row fill-height wrap>
      <v-flex xs12>
        <div>
          <v-img
            floating
            aspect-ratio="1"
            max-height="400"
            transition="scale-transition"
            width="auto"
            min-height="200"
            contain
            :src="require('~/assets/imgs/LOGO.png')"
            position="center center"
          ></v-img>
        </div>
      </v-flex>
      <v-flex xs12 text-xs-center style="padding:2px 2px 2px 2px; min-width:300px;">
        <div>
          <v-card flat color="rgb(0,0,0,0)">
            <v-card-title >
              <div>
                <div
                  style="border-style:solid; border-color:#01ffff; color:#01ffff;"
                  class="display-1 thaifont"
                >เเนะนำค่าย</div>
                <br>
                <span
                  class="title thaifont"
                  style="color:#b9cbff"
                >CS Camp XI หรือ CS Camp ครั้งที่ 11 เป็นค่ายวิทยาการคอมพิวเตอร์ ของภาควิชาวิทยาการคอมพิวเตอร์ สถาบันเทคโนโลยี พระจอมเกล้าเจ้าคุณทหารลาดกระบัง โดยภายในค่ายครั้งนี้ จะมีกิจกรรมต่างๆ เพื่อทำให้ผู้เข้าร่วม ได้เข้าใจคำว่า “วิทยาการคอมพิวเตอร์” มากขึ้น พร้อมด้วยคณะอาจารย์ และพี่ๆ ภายในภาควิชา มาให้คำแนะนำผู้เข้าร่วมอย่างดี</span>
              </div>
            </v-card-title>
          </v-card>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>