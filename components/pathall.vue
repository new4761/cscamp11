<template>
  <v-container fill-height fluid grid-list-xl>
    <v-flex
      xs12
      sm8
      offset-sm2
      text-xs-center
      style="border-style:solid; border-color:#01ffff; color:#01ffff;"
    >
      <v-flex xs12>
        <br>
        <div class="display-1 thaifont">วิธีการเดินทางมายังค่าย</div>
      </v-flex>
      <br>

      <v-expansion-panel focusable>
        <v-expansion-panel-content
          v-for="(pathMap,i) in pathMap"
          :key="i"
          :prepend-icon="pathMap.icon"
          style="background-color:rgba(255, 0, 0, 0.0 ); "
        >
          <div style="color:#01ffff;  " slot="header">
            <v-icon style="color:#01ffff;">{{pathMap.icon}}</v-icon>
            {{ pathMap.name }}
          </div>
          <v-card v-for=" more in pathMap.more" :key="more.text" style="background-color:#018989 ;">
            <v-card-text>{{ more.text }}</v-card-text>
          </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-flex>
  </v-container>
</template>
<style>
</style>

<script>
export default {
  data: () => ({
    pathMap: [
      {
        //cscamp

        name: "รถยนต์ส่วนตัว",
        more: [
          {
            text:
              "เริ่มจากกรุงเทพฯ ออกทางจากถนนมอเตอร์เวย์ กรุงเทพฯ-ชลบุรี-สายใหม่ออกจากมอเตอร์เวย์ ที่ กม 16 กลับรถใต้สะพาน เลี้ยวซ้ายเข้าถนน ฉลองกรุง ตรงมาเรื่อยๆ ผ่าน คณะเทคโนโลยีการเกษตร คณะคุรุอุตสาหกรรม คณะวิทยาศาสตร์จะอยู่ทางด้านซ้าย"
          },
          {
            text:
              "เริ่มจากชลบุรี เริ่มจากเส้นทางพิเศษบูรวิถี ขับตรงมาเรื่อยๆ ชิดซ้ายเพื่อใช้เส้นทางไปสนามบินสุววรณภูมิ (ถนนนท่าอากาศยานสุวรรณภูมิ 3) ขับตรงมาเรื่อยๆ เลี้ยวขวาเข้าสู่ถนนสุววรณภูมิ 2 เลี้ยวขวา เข้าสู่ถนนลาดกระบังเเล้วให้ชิดซ้ายโดยใช้สะพานเล็กๆ ผ่านคณะเทคโนโลยีการเกษตร คณะวิศวกรรมศาสตร์ ข้ามทางรถไฟ คณะวิทยาศาสตร์"
          }
        ],
        show: false,
        icon: "directions_car"
      },
      {
        //cscamp

        name: "รถไฟไทย",
        more: [
          {
            text:
              "จากหัวลำโพง ขบวนเเละเวลาออก 275(05:55),285(06:55),281(08:00),367(10:10)  ลาดกระบัง ลงป้ายหยุดรถพระจอมเกล้า ค่าโดยสาร ฟรี"
          }
        ],
        show: false,
        icon: "directions_railway"
      },
      {
        //cscamp

        name: "รถตู้",
        more: [
          {
            text:
              "สาย เดอะมอล์บางกะปิ-สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง ราคาประมาณ 25บาท ลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ ต.144 สถานีขนส่งผู้โดยสารหมอชิตใหม่(จตุจักร)-สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารบาดกระบังเดินข้ามสะพานลอยหน้าสถานี เดินมาตามทางเท้า ท่ารถตู้จะอยู่ทางซ้าย ค่าโดยสาร 45บาทลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ ต.156 อนุสาวรีย์ชัยสมรภูมิ - สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบังท่ารถตู้อยู่บริเวณเกาะดินเเดง ค่าโดยสาร 40 บาทลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ 554ศูนย์การค้าฟิวเจอร์พาร์ครังสิต - สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบังค่าโดยสาร 60 บาท ท่ารถตู้อยู่ระหว่างโรบินสัน บิ๊กซี เเละโฮมโปร ลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ ต.23 มีนบุรี - สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบัง-หัวตะเข้ลงหน้าคณะวิทยาศาสตร์ ค่าโดย สาร20บาท"
          },
          {
            text:
              "สายที่ ต.50 ซีคอนสเเควร์-หัวตะเข้ ค่าโดยสาร 20 บาท นั่งมาสุดสาย เเล้วต่อรถมาลงตรงข้ามคณะวิทยาศาสตร์ โดยรถสองเเถวที่เขียวว่าผ่านเทคโนโลยี"
          }
        ],
        show: false,
        icon: "local_taxi"
      },
      {
        //cscamp

        name: "แอร์พอตลิ้ง",
        more: [
          {
            text:
              "จากพญาไท  หัวหมากบ้านทับช้างลงสถานีลาดกระบัง - ต่อ รถสองเเถว สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง(ค่าโดยสาร 7 บาท)ลงตรงข้ามคณะวิทยาศาสตร์"
          }
        ],
        show: false,
        icon: "tram"
      },
      {
        //cscamp

        name: "รถประจำทาง",
        more: [
          {
            text:
              "สาย เดอะมอล์บางกะปิ-สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง ราคา 25 บาท ลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ ต.144 สถานีขนส่งผู้โดยสารหมอชิตใหม่(จตุจักร)- สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารบาดกระบังเดินข้ามสะพานลอยหน้าสถานีเดินมาตามทางเท้า ท่ารถตู้จะอยู่ทางซ้าย ค่าโดยสาร 45 บาทลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              " สายที่ ต.156 อนุสาวรีย์ชัยสมรภูมิ - สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบังท่ารถตู้อยู่บริเวณเกาะดินเเดง ค่าโดยสาร 40 บาทลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              "สายที่ 554ศูนย์การค้าฟิวเจอร์พาร์ครังสิต -สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบังค่าโดยสาร 60 บาท ท่ารถตู้อยู่ระหว่างโรบินสัน บิ๊กซี เเละโฮมโปรลงตรงข้ามคณะวิทยาศาสตร์"
          },
          {
            text:
              " สายที่ ต.23 มีนบุรี -สถาบันเทคโนโลยีพระจอมเกล้าคุณทหารลาดกระบัง-หัวตะเข้ลงหน้าคณะวิทยาศาสตร์ค่าโดย สาร20บาท"
          },
          {
            text:
              " สายที่ ต.50 ซีคอนสเเควร์-หัวตะเข้ ค่าโดยสาร 20 บาท นั่งมาสุดสายเเล้วต่อรถมาลงตรงข้ามคณะวิทยาศาสตร์โดยรถสองเเถวที่เขียวว่าผ่านเทคโนโล"
          },
          {
            text:
              " สาย เดอะมอล์บางกะปิ-สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง ราคาประมาณ 25บาท ลงตรงข้ามคณะวิทยาศาสตร์"
          }
        ],
        show: false,
        icon: "directions_bus"
      },
      {
        //cscamp

        name: "พี่ไปรับตามจุดต่างๆ",
        more: [
          { text: "อนุสาวรีย์ชัยสมรภูมิ" },
          { text: "สถานีขนส่งหมอชิต" },
          { text: "สถานีรถไฟหัวลำโพง" },
          { text: "แอร์พอตลิ้ง สถานีลาดกระบัง" }
        ],
        show: false,
        icon: "pin_drop"
      }
    ]
  }),
  methods: {
    getImgUrl(pet) {
      var images = require.context("../assets/imgs", false);
      return images("./" + pet);
    }
  }
};
</script>