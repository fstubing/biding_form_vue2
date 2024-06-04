<template>
  <div class="row g-4 mt-5">
    <div class="col-5 p-4 border border-secondary rounded bg-dark">
      <form action="">
        <div class="row mb-3">
          <label for="titulo" class="col-sm-2 col-form-label text-secondary"
            >Título</label
          >
          <div class="col-sm-6">
            <input
              type="text"
              class="form-control form-control-sm"
              id="titulo"
              name="titulo"
              v-model="formulario.titulo"
            />
          </div>
        </div>
        <hr class="border border-secondary" />
        <div class="row mb-3">
          <label for="inputState" class="col-sm-2 col-form-label text-secondary"
            >Emoji</label
          >
          <div class="col-sm-3">
            <select
              id="inputState"
              class="form-select"
              v-model="formulario.emoji"
            >
              <option value="&#128110;" selected>&#128110;</option>
              <option value="&#128119;">&#128119;</option>
              <option value="&#128131;">&#128131;</option>
              <option value="&#129495;">&#129495;</option>
              <option value="&#128586;">&#128586;</option>
            </select>
          </div>
        </div>
        <hr class="border border-secondary" />
        <div class="row mb-3">
          <div class="col-sm-2">
            <span class="text-secondary pe-3">Apreciación: </span>
          </div>
          <div class="col-sm-10">
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio1"
                value="Regular"
                v-model="formulario.apreciacion"
              />
              <label class="form-check-label text-secondary" for="inlineRadio1"
                >Regular</label
              >
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio2"
                value="Bien"
                v-model="formulario.apreciacion"
              />
              <label class="form-check-label text-secondary" for="inlineRadio2"
                >Bien</label
              >
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio3"
                value="Muy Bien"
                v-model="formulario.apreciacion"
              />
              <label class="form-check-label text-secondary" for="inlineRadio4"
                >Muy Bien</label
              >
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio4"
                value="Increible"
                v-model="formulario.apreciacion"
              />
              <label class="form-check-label text-secondary" for="inlineRadio4"
                >Increible</label
              >
            </div>
          </div>
        </div>
        <hr class="border border-secondary" />
        <div class="row mb-3">
          <div class="col-sm-2">
            <span class="text-secondary pe-3">Competencias Aprendidas:</span>
          </div>
          <div class="col-sm-8 ms-5">
            <div class="row">
              <div class="form-check form-check-inline col-5 mb-2">
                <input
                  class="form-check-input"
                  type="checkbox"
                  id="inlineCheckbox1"
                  value="Morfología de un Componente"
                  v-model="formulario.competencias"
                />
                <label
                  class="form-check-label text-secondary"
                  for="inlineCheckbox1"
                  >Morfología de un Componente</label
                >
              </div>
              <div class="form-check form-check-inline col-5 mb-2">
                <input
                  class="form-check-input"
                  type="checkbox"
                  id="inlineCheckbox2"
                  value="Directivas"
                  v-model="formulario.competencias"
                />
                <label
                  class="form-check-label text-secondary"
                  for="inlineCheckbox2"
                  >Directivas</label
                >
              </div>
              <div class="form-check form-check-inline col-5 mb-2">
                <input
                  class="form-check-input"
                  type="checkbox"
                  id="inlineCheckbox3"
                  value="One-Way y Two-Way data binding"
                  v-model="formulario.competencias"
                />
                <label
                  class="form-check-label text-secondary"
                  for="inlineCheckbox3"
                  >One-Way y Two-Way data binding</label
                >
              </div>
              <div class="form-check form-check-inline col-5 mb-2">
                <input
                  class="form-check-input"
                  type="checkbox"
                  id="inlineCheckbox4"
                  value="Estado"
                  v-model="formulario.competencias"
                />
                <label
                  class="form-check-label text-secondary"
                  for="inlineCheckbox4"
                  >Estado</label
                >
              </div>
              <div class="form-check form-check-inline col-5 mb-2">
                <input
                  class="form-check-input"
                  type="checkbox"
                  id="inlineCheckbox5"
                  value="Patrón de diseño MVVM"
                  v-model="formulario.competencias"
                />
                <label
                  class="form-check-label text-secondary"
                  for="inlineCheckbox5"
                  >Patrón de diseño MVVM</label
                >
              </div>
            </div>
          </div>
        </div>
        <hr class="border border-secondary" />
        <div class="row mb-3">
          <label
            for="exampleFormControlTextarea1"
            class="form-label text-secondary col-sm-2"
            >Opinión:
          </label>
          <div class="col-sm-10">
            <textarea
              class="form-control"
              id="exampleFormControlTextarea1"
              rows="2"
              v-model="formulario.opinion"
            ></textarea>
          </div>
        </div>
      </form>
    </div>
    <div class="col-7 p-4 border border-secondary rounded">
      <p style="font-size: 50px" class="text-center">{{ formulario.emoji }}</p>
      <h3 class="text-center text-secondary">{{ formulario.titulo }}</h3>
      <p class="text-center text-secondary">
        Y me parece {{ formulario.apreciacion }}
      </p>
      <p class="text-center text-secondary">He aprendido:</p>
      <p class="text-center text-secondary">{{ formulario.competencias }}</p>
      <p class="text-center text-secondary">
        Mi opinión hasta ahora del framework es:
      </p>
      <p class="text-center text-secondary">{{ formulario.opinion }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formulario: {
        emoji: "",
        titulo: "",
        apreciacion: "",
        competencias: [],
        opinion: "",
      },
    };
  },
};
</script>

<style></style>
