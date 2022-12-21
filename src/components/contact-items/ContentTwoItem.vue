<template>
    <div class="write-content">
        <h3>Напишите Нам</h3>
        <div class="write-wrapper">
            <input type="text" class="name input" placeholder="ФИО">
            <input type="text" class="mail input" placeholder="Электронная почта">
            <input type="text" class="title input" placeholder="Тема">
            <textarea name="" id="" cols="30" rows="10" class="descript input" placeholder="Текст сообщения"></textarea>
            <!-- //TODO Recaptcha -->
            <div class="captcha"></div>
            <button class="send-btn">Отправить</button>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>