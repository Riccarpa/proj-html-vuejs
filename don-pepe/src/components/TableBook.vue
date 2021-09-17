<template>
  <section>
    <div class="container h-100">
      <div class="row h-100">
        <div class="col h-100 d-flex justify-content-center align-items-center">
          <select>
            <option selected>1 person</option>
            <option value="1">2 people</option>
            <option value="2">3 people</option>
            <option value="3">4 people</option>
          </select>
          <span class="ms-3 me-3 text-white">FOR</span>
          <input type="date" />
          <span class="ms-3 me-3 text-white">AT</span>
          <input type="time" value="12:55" />
          <button type="button" class="btn btn-danger">
            BOOK A TABLE
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TableBook",
};
</script>

<style lang="scss" scoped>
section {
  margin-bottom: 0.5rem;
  height: 200px;
  background-image: url("../img/h3-background-img-3.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
select,
input {
  padding: 0.5rem;
  border: 2px solid black;
}
button {
  padding: 1rem;
  border-radius: 0;
  width: 100px;
  font-size: 9px;
  margin-left: 6rem;
  border: 2px solid black;
}
</style>
