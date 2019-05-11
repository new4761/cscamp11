<template>
  <v-container grid-list-sm>
    <v-layout align-center justify-center>
      <v-flex xs12>
        <div class="text-xs-center">
          <v-dialog v-model="dialog" width="600">
            <v-btn slot="" outline color="light-green accent-3" large disabled>
              <v-icon>edit</v-icon>ลงทะเบียน
            </v-btn>

            <v-card flat class="light-blue darken-4">
              <v-card-title
                class="headline cyan darken-2 thaifont cyan--text text--lighten-4"
                primary-title
              >
                <strong>
                  <v-icon class="pr-1" large color="#B2EBF2">assignment_ind</v-icon>คุณสมบัติของผู้สมัคร
                </strong>
              </v-card-title>

              <v-card-text class="light-blue darken-2 thaifont cyan--text text--lighten-4">
                <ul>
                  <li>
                    1. เป็นนักเรียนระดับมัธยมศึกษาระหว่างปีที่ 4 หรือ 5 ในปีการศึกษา 2561 แผนการเรียนเน้นวิทยาศาสตร์
                    ทุกแผนการเรียน ศิลป์-คำนวณ ทุกแผนการเรียน หรือเทียบเท่า
                  </li>
                  <li>2. เป็นผู้ที่ไม่มีโรคติดต่อร้ายแรง โรคที่สังคมรังเกียจ หรือโรคสำคัญที่เป็นอุปสรรคต่อการทำกิจกรรม</li>
                  <li>3. เป็นผู้ที่ไม่มีความผิดปรกติทางร่างกายหรือทางจิตใจ ซึ่งอาจก่อให้เกิดอุปสรรคต่อการเข้าร่วมกิจกรรมหรือละเมิดสิทธิของผู้อื่น</li>
                  <li>4. ไม่เคยเข้าร่วมค่ายฝึกอบรมเชิงปฏิบัติการวิทยาการคอมพิวเตอร์ ณ สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง มาก่อน</li>
                  <li>
                    5. สามารถเข้าร่วมกิจกรรมค่ายพักแรม ณ สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง
                    ระหว่างวันที่ 31 พฤษภาคม - 2 มิถุนายน พุทธศักราช 2562 ได้
                  </li>
                </ul>
              </v-card-text>

              <v-card-title
                class="headline cyan darken-2 thaifont cyan--text text--lighten-4"
                primary-title
              >
                <strong>
                  <v-icon class="pr-1" large color="#B2EBF2">gavel</v-icon>กติกาการคัดเลือกผู้สมัคร
                </strong>
              </v-card-title>

              <v-card-text class="light-blue darken-2 thaifont cyan--text text--lighten-4">
                <ul>
                  <li>
                    1. ผู้สมัครมีคุณสมบัติครบถ้วนตามที่ได้ระบุไว้ข้างต้น กรอกเอกสารการสมัครออนไลน์ถูกต้อง ผ่านทางเว็บไซต์
                    cs-camp.net ภายในวันที่ 28 เมษายน พุทธศักราช 2562
                  </li>
                  <li>2. ผู้สมัครต้องตอบคำถามสำหรับการคัดเลือกครบทุกคำถาม</li>
                </ul>
              </v-card-text>
              <v-card-title
                class="headline cyan darken-2 thaifont cyan--text text--lighten-4"
                primary-title
              >
                <strong>
                  <v-icon class="pr-1" large color="#B2EBF2">assignment_turned_in</v-icon>เกณฑ์การให้คะแนนคัดเลือกผู้สมัคร
                </strong>
              </v-card-title>

              <v-card-text class="light-blue darken-2 thaifont cyan--text text--lighten-4">
                <ul>
                  <li>
                    1. ผู้สมัครจะได้รับลำดับในการพิจารณาการคัดเลือก การพิจารณาผู้สมัครจะเป็นไปตามลำดับที่สมัครก่อนเสมอ
                    หากม  ีผู้ที่ได้รับการคัดเลือกครบตามจำนวนที่รับสมัคร (100 คน) ลำดับต่อไปจะถูกพิจารณาเป็นรายชื่อสำรอง
                  </li>
                  <li>2. ผู้สมัครที่ไม่ปฏิบัติตามกติกาการคัดเลือก จะถือว่าการสมัครเป็นโมฆะ</li>
                  <li>3. ผู้สมัครจะถูกคัดเลือกจากคำตอบของคำถามเป็นจำนวน 5 คำถาม คิดเป็นคะแนนสะสมรวมทั้งสิน 500 คะเเนนผู้สมัครทีได้รับคะเนนสะสมตั้งเเต่ 350 คะเเนนขึ้นไป จะถือว่าผ่านเกณฑ์การคัดเลือก</li>
                </ul>
                <div class="text-xs-center">
                  <a
                    href="https://drive.google.com/file/d/1KMHxnQIoVrDqyPeJ9b5TsXqz80xfWNFn/view?usp=sharing"
                    target="_blank"
                    style="   text-decoration: none;"
                  >
                    <v-btn color="amber darken-2 white--text " round large>
                      <v-icon class="pr-1">assignment_turned_in</v-icon>เงื่อนไขการรับสมัครฉบับเต็ม
                    </v-btn>
                  </a>
                </div>
              </v-card-text>

              <v-divider></v-divider>

              <v-card-actions>
                <v-btn color="#29B6F6" disabled block href="#">
                  <v-icon class="pr-1">check_circle</v-icon>ข้าพเจ้ายอมรับข้อตกลง
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
          <a
            href="https://drive.google.com/file/d/1KMHxnQIoVrDqyPeJ9b5TsXqz80xfWNFn/view?usp=sharing"
            target="_blank"
          >
            <v-btn outline color="amber darken-1" large>
              <v-icon class="pr-1">assignment_turned_in</v-icon>เงื่อนไขการรับสมัคร
            </v-btn>
          </a>
          <v-btn outline color="yellow darken-1" @click="$vuetify.goTo('#date')" large>
            <v-icon class="pr-1">schedule</v-icon>กำหนดการ
          </v-btn>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      dialog: false
    };
  }
};
</script>
