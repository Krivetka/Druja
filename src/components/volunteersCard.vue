<template>
  <div class="card">
    <div class="slider">
      <div class="person-info">
        <div class="filter"></div>
        <img
            class="photo"
            v-bind:src="active_photo"/>
        <div class="content">
          <h2>{{active_name}}</h2>
          <p>Волонтер</p>
          <p>В проэкте {{active_in_project}} лет</p>
          <p>{{active_text}}</p>
          <div class="links">
          </div>
        </div>
      </div>
    </div>
    <div class="nav-slider">
      <div class="person" v-for="user in Users" :key="user.name"
           @click="setData(user.background,user.photo,user.name,user.age,user.age_in_project,user.text)">
        <div class="container">
          <div class="container-inner">
            <img
                class="circle"
                v-bind:src="user.background"
            />
            <img
                class="img"
                v-bind:style="user.photo_style"
                v-bind:src="user.photo"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'volunteersCard',
  data() {
    return {
      background_img: '',
      active_photo: 'src/assets/person0.png',
      active_name: 'Александр Плыгавко',
      active_age: '',
      active_in_project: '100',
      active_text: '\"Хотите отдохнуть вдалеке от шумного города, насладится природой и спокойствием?\n' +
          'Тогда к нам!\"',
      Users: [
        {
          photo_style: '  left: 22px; top: 164px; width: 340px;',
          background: 'https://phonoteka.org/uploads/posts/2022-02/1644932016_32-phonoteka-org-p-zheltii-fon-akvarel-33.jpg',
          photo: "src/assets/person0.png",
          name: 'Александр Плыгавко',
          age: '12',
          age_in_project: '100',
          text: '\"Хотите отдохнуть вдалеке от шумного города, насладится природой и спокойствием?\n' +
              'Тогда к нам!\"'
        },
        {
          photo_style: 'left: -46px; top: 174px; width: 444px;',
          background: 'https://top-fon.com/uploads/posts/2023-01/1674963706_top-fon-com-p-mramornii-fon-dlya-prezentatsii-pastelnii-1.jpg',
          photo: "src/assets/person2.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: 'left: -16px; top: 144px; width: 466px;',
          background: 'https://catherineasquithgallery.com/uploads/posts/2021-02/1612772032_122-p-fon-akvarelnii-rozovo-goluboi-190.jpg',
          photo: "src/assets/person3.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: '  left: 22px; top: 164px; width: 340px;',
          background: 'https://phonoteka.org/uploads/posts/2022-02/1644932016_32-phonoteka-org-p-zheltii-fon-akvarel-33.jpg',
          photo: "src/assets/person1.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: 'left: -46px; top: 174px; width: 444px;',
          background: 'https://top-fon.com/uploads/posts/2023-01/1674963706_top-fon-com-p-mramornii-fon-dlya-prezentatsii-pastelnii-1.jpg',
          photo: "src/assets/person2.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        }
        ,
        {
          photo_style: 'left: -16px; top: 144px; width: 466px;',
          background: 'https://catherineasquithgallery.com/uploads/posts/2021-02/1612772032_122-p-fon-akvarelnii-rozovo-goluboi-190.jpg',
          photo: "src/assets/person3.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: '  left: 22px; top: 164px; width: 340px;',
          background: 'https://phonoteka.org/uploads/posts/2022-02/1644932016_32-phonoteka-org-p-zheltii-fon-akvarel-33.jpg',
          photo: "src/assets/person1.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: 'left: -46px; top: 174px; width: 444px;',
          background: 'https://top-fon.com/uploads/posts/2023-01/1674963706_top-fon-com-p-mramornii-fon-dlya-prezentatsii-pastelnii-1.jpg',
          photo: "src/assets/person2.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        }
        ,
        {
          photo_style: 'left: -16px; top: 144px; width: 466px;',
          background: 'https://catherineasquithgallery.com/uploads/posts/2021-02/1612772032_122-p-fon-akvarelnii-rozovo-goluboi-190.jpg',
          photo: "src/assets/person3.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: '  left: 22px; top: 164px; width: 340px;',
          background: 'https://phonoteka.org/uploads/posts/2022-02/1644932016_32-phonoteka-org-p-zheltii-fon-akvarel-33.jpg',
          photo: "src/assets/person1.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
        {
          photo_style: 'left: -46px; top: 174px; width: 444px;',
          background: 'https://top-fon.com/uploads/posts/2023-01/1674963706_top-fon-com-p-mramornii-fon-dlya-prezentatsii-pastelnii-1.jpg',
          photo: "src/assets/person2.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        }
        ,
        {
          photo_style: 'left: -16px; top: 144px; width: 466px;',
          background: 'https://catherineasquithgallery.com/uploads/posts/2021-02/1612772032_122-p-fon-akvarelnii-rozovo-goluboi-190.jpg',
          photo: "src/assets/person3.png",
          name: 'Ghfe GHJ',
          age: '12',
          age_in_project: '2',
          text: 'text'
        },
      ]
    }
  },
  methods: {
    setData(background_img,
            active_photo,
            active_name,
            active_age,
            active_in_project,
            active_text) {
      this.background_img = background_img;
      this.active_photo = active_photo;
      this.active_name = active_name;
      this.active_age = active_age;
      this.active_in_project = active_in_project;
      this.active_text = active_text;
    }
  }
}
</script>

<style scoped>
.card {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 100%;
  height: 100vh;
}

.person-info {
  position: relative;
  width: 50vw;
  height: 56vh;
  border-radius: 20px;
  background: url("@/assets/photo/1.jpg");
  background-size: contain;
  box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
}

.photo {
  position: absolute;
  bottom: 0;
  left: 3vw;
  height: 90%;
}

.filter {
  border-radius: 20px;
  backdrop-filter: blur(7px);
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}

.content {
  position: absolute;
  right: 20px;
  top: -10px;
  width: 20vw;
  height: calc(100% + 30px);
  padding: 30px;
  background: #fff;
  box-shadow: 0 2px 8px rgba(55, 55, 55, .3);
  border-radius: 5px;
}

h2 {
  color: #444;
  font-size: 26px;
}

p {
  color: #999;
}


.nav-slider {
  display: flex;
  align-items: center;
  justify-content: start;
  width: 70vw;
  overflow: hidden;
  margin-bottom: -70px;
}

.person {
  scale: 0.6;
  align-items: center;
  display: flex;
  flex-direction: column;
  width: 140px;
  cursor: pointer;
}

.container {
  border-radius: 50%;
  height: 312px;
  -webkit-tap-highlight-color: transparent;
  transform: scale(0.48);
  transition: transform 250ms cubic-bezier(0.4, 0, 0.2, 1);
  width: 400px;
}

.container:hover {
  transform: scale(0.54);
}

.container-inner {
  clip-path: path(
      'M 390,400 C 390,504.9341 304.9341,590 200,590 95.065898,590 10,504.9341 10,400 V 10 H 200 390 Z'
  );
  position: relative;
  transform-origin: 50%;
  top: -200px;
}

.circle {
  background-color: #fee7d3;
  border-radius: 50%;
  cursor: pointer;
  height: 380px;
  left: 10px;
  pointer-events: none;
  position: absolute;
  top: 210px;
  width: 380px;
}

.img {
  pointer-events: none;
  position: relative;
  transform: translateY(20px) scale(1.15);
  transform-origin: 50% bottom;
  transition: transform 300ms cubic-bezier(0.4, 0, 0.2, 1);
}

.container:hover .img {
  transform: translateY(0) scale(1.2);
}
</style>
