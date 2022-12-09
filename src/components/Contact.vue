<script>

</script>
<template>
    <div class="container">
        <form>
            <div class="section">
                <h3>Contactame</h3>
                <label><img src="https://res.cloudinary.com/difrw7gue/image/upload/v1670601169/icons8-name-tag-24_xr7nzx.png"></label>
                <input type="text" id="name" class="inputElement" required placeholder="nombre">
            </div>
            <div class="section">
                <label><img src="https://res.cloudinary.com/difrw7gue/image/upload/v1670601169/icons8-mail-24_qcrywn.png"></label>
                <input type="email" id="email" class="inputElement" required placeholder="Correo electrónico">
            </div>
            <div class="section">
                <label><img src="https://res.cloudinary.com/difrw7gue/image/upload/v1670601169/icons8-composing-mail-24_aylxil.png"></label>
                <textarea type="text" id="email" class="areaElement" required placeholder="Mensaje"></textarea>
            </div>
            <div class="section">
                <input type="submit" class="submitElement">
            </div>
        </form>
    </div>
</template>

<style scoped>
.section{
    margin: auto;
    width: 90%;
    text-align: center;
}
.container{
    background-color: #222225;
    height: 400px;
    margin: auto;
    padding: 50px;
    color: rgb(226, 207, 207);
    overflow: hidden;
    margin-bottom: 50px;
}
.inputElement{
    margin: 10px;
    border-top-style: hidden;
    border-right-style: hidden;
    border-left-style: hidden;
    border-bottom-style: groove;
    background-color: rgb(14, 14, 15);
    width: 90%;
    padding: 10px;
    color: rgb(226, 207, 207);
}

.areaElement{
    margin: 10px;
    border-top-style: hidden;
    border-right-style: hidden;
    border-left-style: hidden;
    border-bottom-style: groove;
    background-color: rgb(14, 14, 15);
    width: 90%;
    padding: 10px;
    color: rgb(226, 207, 207);
}

.submitElement{
    background-color: rgb(228, 151, 9);
    border-style: none;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 5px;
    padding-bottom: 5px;
}

.inputElement:focus {
        outline: none;
}

img{
    width: 30px;
    height: 30px;
}

</style>
  