<script>

</script>
<template>
<div class="container contact-form">
            <div class="contact-image">
                <img src="https://res.cloudinary.com/difrw7gue/image/upload/v1670565373/rocket_contact_zzke7p.png" alt="rocket_contact"/>
            </div>
            <form>
                <h3>Contactame</h3>
               <div class="row">
                    <div class="f1">
                        <div class="form-group">
                            <input type="text" name="txtName" class="form-control" placeholder="Nombre" value="" />
                        </div>
                        <div class="form-group">
                            <input type="text" name="txtEmail" class="form-control" placeholder="Correo" value="" />
                        </div>
                        <div class="form-group">
                            <input type="text" name="txtEmail" class="form-control" placeholder="Asunto" value="" />
                        </div>
                    </div>
                    <div class="f2">
                        <div class="form-group">
                            <textarea name="txtMsg" class="form-control" placeholder="Mensaje" style="width: 100%; height: 150px;"></textarea>
                        </div>
                    </div>
                    <div class="form-group">
                            <input type="submit" name="btnSubmit" class="btnContact" value="Send Message" />
                    </div>
                </div>
            </form>
</div>
</template>

<style scoped>
.f1{
    display: flex;
}
.form-group{
    margin: 10px;
}
.container{
    color: rgb(226, 207, 207);
    text-align: center;
}
.contact-form{
    background: rgb(33, 33, 36);
    margin-top: 30px;
    margin-bottom: 5%;
    width: 70%;
}
.contact-image{
    text-align: center;
}
.contact-image img{
    border-radius: 6rem;
    width: 11%;
    margin-top: -3%;
    transform: rotate(29deg);
}
.contact-form form{
    padding: 50px;
}
.contact-form form .row{
    margin-bottom: 7%;
}
.contact-form h3{
    margin-bottom: 8%;
    text-align: center;
    margin-top: -50px;
}
.contact-form .btnContact {
    width: 50%;
    border: none;
    padding: 1.5%;
    background:  rgb(228, 151, 9);
    font-weight: 600;
    color: #fff;
    cursor: pointer;
}

</style>
  