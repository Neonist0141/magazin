<!-- Footer.vue -->

<template>
    <footer>
      <div class="footer-content">
        <div class="contact-info">
          <p>Телефон: {{ phoneNumber }}</p>
          <p>Юридический адрес: {{ legalAddress }}</p>
        </div>
        <div class="social-links">
          <a href="https://vk.com/anatoliysvet" target="_blank" rel="noopener noreferrer"><img src="../assets/vk-logo.svg" alt="Вконтакте" style="height: 32px;"></a>
          <a href="https://t.me/AnatSvet" target="_blank" rel="noopener noreferrer"><img src="../assets/telegram-logo.svg" alt="Телеграм" style="height: 32px;"></a>
          <a href="https://github.com/Neonist0141" target="_blank" rel="noopener noreferrer"><img src="../assets/github-logo.svg" alt="Github" style="height: 32px;"></a>
        </div>
      </div>
      <p>&copy; 2023 Магазин рукодельных изделий "Сделай сам". Все права защищены.</p>
    </footer>
</template>
  
<script>
  export default {
    name: 'Footer-component',
    data() {
      return {
        phoneNumber: '+7 (999) 515-7450', // Замените на ваш номер телефона
        legalAddress: 'г. Гатчина', // Замените на ваш юридический адрес
      };
    },
  };
  </script>
  
  <style scoped>
  /* Стили для вашего футера */
  footer {
    text-align: center;
    padding: 20px;
  }
  
  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .social-links {
    display: flex;
    gap: 0.5cm;
  }
  .contact-info {
    text-align: left;
  }
</style>
  
