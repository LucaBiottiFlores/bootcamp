<template>
<div class="container mt-5 pt-5">
<table class="table table-hover table-striped">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">Nombre</th>
        <th scope="col">Apellido</th>
        <th scope="col">RUT</th>
        <th scope="col">Edad</th>
        <th scope="col">Fecha de Nacimiento</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(persona, $index) of personas" :key="$index">
        <td>{{ $index }}</td>
        <td>{{ persona.nombre }}</td>
        <td>{{ persona.apellido }}</td>
        <td>{{ persona.rut }}</td>
        <td>{{ persona.edad }}</td>
        <td>{{ persona.fechaDeNacimiento }}</td>
      </tr>
    </tbody>
  </table>
</div>
  
</template>

<script>


export default {
  name: "App",
  data: () => ({
    personas: [
      {
        nombre: "Angelica",
        apellido: "Vidal",
        rut: "1.234.567-8",
        edad: 20,
        fechaDeNacimiento: "01-01-2000",
      },
      {
        nombre: "Gonzalo",
        apellido: "Trujillo",
        rut: "1.234.567-8",
        edad: 20,
        fechaDeNacimiento: "01-01-2000",
      },
      {
        nombre: "Sebastian",
        apellido: "Gomez",
        rut: "1.234.567-8",
        edad: 20,
        fechaDeNacimiento: "01-01-2000",
      },
      {
        nombre: "Luis",
      },
    ],
  }),
};
</script>

<style>

  .table {
background: rgba( 255, 255, 255, 0.30 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 5.5px );
-webkit-backdrop-filter: blur( 5.5px );
border-radius: 10px;
  }

</style>
