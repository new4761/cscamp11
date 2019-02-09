<template>
  <v-container grid-list-sm class=".headimg">
    <v-layout align-center justify-center row fill-height text-xs-left>
      <v-flex xs7 offset-sm1>
        <div>
          <v-card color="blue-grey" dark tile flat>
            <v-card-text
              justify-center
              align-center
              class="thaifont text-truncate text-lg-left"
              style=" float:right;"
            >
              <h4 style="font-size:2vw;" contain>
                <p style="text-decoration: underline; ">CSCAMP คืออะไร</p>
              </h4>
              <v-spacer></v-spacer>
              <h6
                style="font-size:1vw;"
              >CS Camp XI หรือ CS Camp ครั้งที่ 11 เป็นค่ายวิทยาการคอมพิวเตอร์ ของภาควิชาวิทยาการคอมพิวเตอร์
                <br>สถาบันเทคโนโลยี พระจอมเกล้าเจ้าคุณทหารลาดกระบัง โดยภายในค่ายครั้งนี้ จะมีกิจกรรมต่างๆ
                <br>เพื่อทำให้ผู้เข้าร่วม ได้เข้าใจคำว่า “วิทยาการคอมพิวเตอร์” มากขึ้น พร้อมด้วยคณะอาจารย์ และพี่ๆ
                <br>ภายในภาควิชา มาให้คำแนะนำผู้เข้าร่วมอย่างดี
              </h6>
            </v-card-text>
          </v-card>
        </div>
      </v-flex>
      <v-flex xs5>
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
            position="center left"
          ></v-img>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>