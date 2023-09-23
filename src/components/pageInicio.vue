<template>
  <div class="profile-section">
    <div class="profile-content">
      <div class="profile-details">
        <p class="profile-name">¡Hola! Soy</p>
        <h1 class="profile-titulo">Jeremías Torres</h1>
        <p class="profile-description text-h6 white--text">
          Soy un desarrollador web con experiencia en diversas tecnologías. Mi
          compromiso es crear soluciones web efectivas y atractivas.
        </p>
      </div>
      <div class="profile-image">
        <img src="../assets/perfil3.png" alt="Imagen de perfil" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pdfUrl: "/my-app/public/Currículum jeremias torres .pdf",
    };
  },
};
</script>

<style>
.profile-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: rgb(29, 48, 66);
  padding: 20px;
  text-align: center;
}

.profile-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 800px;
  width: 100%;
}

.profile-details {
  padding-right: 20px;
  text-align: center;
}

.profile-name {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: white;
}
.profile-titulo {
  font-size: 3rem;
  margin-bottom: 10px;
  color: #ffa726;
}

.profile-description {
  font-size: 1.2rem;
  margin-bottom: 20px;
  color: white;
}

.profile-image img {
  max-width: 200px;
  border-radius: 9%;
  box-shadow: inset 18px 20px #ffa726;
}

.download-button {
  margin-top: 20px;
}
</style>
