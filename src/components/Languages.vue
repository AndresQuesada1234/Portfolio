<script>
export default{
    data(){
        return{
            items: [
            {name: 'HTML', img:'https://res.cloudinary.com/difrw7gue/image/upload/v1670438843/htmlCard_obnwbq.jpg', desc: 'Este lenguaje es fundamental para el desarrollo de software, ya sea en su versión pura o mezclado con otros frameworks. Por esa razón es de los más implementados por mi persona.'},
            {name: 'CSS', img:'https://res.cloudinary.com/difrw7gue/image/upload/v1670438853/cssCard_x2beoh.jpg', desc: 'Para dar estilos a mis aplicaciones, el CSS es de mis favoritos, incluyendo todas sus variantes, y es muy acoplable a distintos framworks.'},
            {name: 'Vue.js', img:'https://res.cloudinary.com/difrw7gue/image/upload/v1670438832/vueCard_aykrfl.webp', desc: 'Su dinamismo y reactividad con el manejo de componentes me gusta mucho, me da la capacidad de hacer aplicaciones muy poderosas.'},
            {name: '.NET', img:'https://res.cloudinary.com/difrw7gue/image/upload/v1670438848/.net_val6vz.png', desc: 'Fundamental para implementaciónes multiplataforma, y gran variedad de frameworks disponibles.'},
            {name: 'C#', img:'https://res.cloudinary.com/difrw7gue/image/upload/v1670438867/c_Card_vhkokn.png', desc: 'De mis lenguajes backend preferidos, la manera en la cual se estructuran los datos y su manejo, da la posibilidad de hacer grandes trabajos.'},
            ]
        }
        
    }
}
</script>
<template>
    <section class="light">
      <div v-for="item in items" class="container py-2">
        <article class="postcard light red">
          <a class="postcard__img_link" href="#">
            <img class="postcard__img" :src="item.img" alt="Image Title" />	
          </a>
          <div class="postcard__text t-dark">
            <h1 class="postcard__title red"><a href="#">{{item.name}}</a></h1>
            <div class="postcard__subtitle small">
            </div>
            <div class="postcard__bar"></div>
            <div class="postcard__preview-txt">{{item.desc}}</div>
          </div>
        </article>
      </div>
    </section>
</template>
<style scoped lang="scss">
$main-green: #79dd09 !default;
$main-green-rgb-015: rgba(121, 221, 9, 0.1) !default;
$main-yellow: #bdbb49 !default;
$main-yellow-rgb-015: rgba(189, 187, 73, 0.1) !default;
$main-red: #bd150b !default;
$main-red-rgb-015: rgba(189, 21, 11, 0.1) !default;
$main-blue: #0076bd !default;
$main-blue-rgb-015: rgba(0, 118, 189, 0.1) !default;

section{
    padding-top: 10px;
}

a, a:hover {
	text-decoration: none;
	transition: color 0.3s ease-in-out;
}

#pageHeaderTitle {
	margin: 2rem 0;
	text-transform: uppercase;
	text-align: center;
	font-size: 2.5rem;
}

/* Cards */
.postcard {
  flex-wrap: wrap;
  display: flex;
  
  box-shadow: 0 4px 21px -12px rgba(0, 0, 0, 0.66);
  border-radius: 10px;
  margin: 0 0 2rem 0;
  overflow: hidden;
  position: relative;
  color: rgb(226, 207, 207);
	&.light {
		background-color: rgb(33, 33, 36);
    margin-top: 30px;
	}
	
  a {
    color: inherit;
  }
	
	h1,	.h1 {
		margin-bottom: 0.5rem;
		font-weight: 500;
		line-height: 1.2;
	}
	
	.small {
		font-size: 80%;
	}

  .postcard__title {
    font-size: 1.75rem;
  }

  .postcard__img {
    max-height: 180px;
    width: 100%;
    object-fit: cover;
    position: relative;
  }

  .postcard__img_link {
    display: contents;
  }

  .postcard__bar {
    width: 50px;
    height: 10px;
    margin: 10px 0;
    border-radius: 5px;
    transition: width 0.2s ease;
  }

  .postcard__text {
    padding: 1.7rem;
    position: relative;
    display: flex;
    flex-direction: column;
  }

  .postcard__preview-txt {
    overflow: hidden;
    text-overflow: ellipsis;
    text-align: justify;
    height: 100%;
    font-size: 1.5em;
  }

  .postcard__tagbox {
    display: flex;
    flex-flow: row wrap;
    font-size: 14px;
    margin: 20px 0 0 0;
		padding: 0;
    justify-content: center;

    .tag__item {
      display: inline-block;
      border-radius: 3px;
      padding: 2.5px 10px;
      margin: 0 5px 5px 0;
      cursor: default;
      user-select: none;

      &:hover {
        background: rgb(33, 33, 36)
      }
    }
  }

  &:before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-image: linear-gradient(-70deg, rgb(33, 33, 36), transparent 50%);
    opacity: 1;
    border-radius: 10px;
  }

  &:hover .postcard__bar {
    width: 100px;
  }
}

@media screen and (min-width: 769px) {
  .postcard {
    flex-wrap: inherit;

    .postcard__title {
      font-size: 2rem;
    }

    .postcard__tagbox {
      justify-content: start;
    }

    .postcard__img {
      max-width: 300px;
      max-height: 100%;
      transition: transform 0.3s ease;
    }

    .postcard__text {
      padding: 3rem;
      width: 100%;
    }

    .postcard__text:before {
      content: "";
      position: absolute;
      display: block;
      background: #18151f;
      top: -20%;
      height: 130%;
      width: 55px;
    }

    &:hover .postcard__img {
      transform: scale(1.1);
    }

    &:nth-child(2n+1) {
      flex-direction: row;
    }

    &:nth-child(2n+0) {
      flex-direction: row-reverse;
    }

    &:nth-child(2n+1) .postcard__text::before {
      left: -12px !important;
      transform: rotate(4deg);
    }

    &:nth-child(2n+0) .postcard__text::before {
      right: -12px !important;
      transform: rotate(-4deg);
    }
  }
}
@media screen and (min-width: 1024px){
		.postcard__text {
      padding: 2rem 3.5rem;
    }
		
		.postcard__text:before {
      content: "";
      position: absolute;
      display: block;
      
      top: -20%;
      height: 130%;
      width: 55px;
    }
	
  .postcard.dark {
		.postcard__text:before {
			background: #18151f;
		}
  }
	.postcard.light {
		.postcard__text:before {
			background: rgb(33, 33, 36);
		}
  }
}

/* COLORS */
.postcard .postcard__tagbox .play:hover {
	background: $main-green;
	color: black;
}
.postcard__title:hover {
	color: $main-green;
}
.postcard__bar {
	background-color: $main-green;
}
.postcard .postcard__tagbox .play:hover {
	background: $main-blue;
}
.postcard__title:hover {
	color: $main-blue;
}
.postcard__bar {
	background-color: $main-blue;
}

.postcard .postcard__tagbox .red.play:hover {
	background: $main-red;
}
.red .postcard__title:hover {
	color: rgb(228, 151, 9);
}
.red .postcard__bar {
	background-color: rgb(228, 151, 9);
}

</style>