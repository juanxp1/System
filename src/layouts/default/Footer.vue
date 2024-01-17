<template>
    <div class="footer">
        <div class="footer-content">
            <p>© 2012 <span>Security Group Website Template</span> by <span>TemplateMonster.com</span></p>
            <p>Phone: +1 800 559 6580 Email: <span>info@security.com</span></p>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.footer {
    background-image: url('@/assets/bg.jpg');
    height: 10rem;
    text-align: center;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    color: white;
}

.footer-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
}

.footer p {
    margin: 5px;
}

span{
    color: #e88800;
}
</style>
