<template>
  <div>
    <PartialsTitle title="HALAMAN MODELING" />
    <textarea v-model="multiline" class="form-control"></textarea>
    <pre>{{multiline}}</pre>

    <section>
      <input type="checkbox" id="checkbox" v-model="checked">
      <label for="checkbox">{{ checked }}</label>
    </section>
    
    <section>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
      <label for="jack">Jack</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames">
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
      <label for="mike">Mike</label>
      <input type="text" id="name" v-model="checkedNames">
      <br>
    </section>
    <span>Checked names: {{ checkedNames }}</span>

    <section>
      <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option value="1">A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <span>Selected: {{ selected }}</span>
    </section>

    <section>
      <label for="provinsi">Provinsi {{provinsi}}</label>
      <select name="" id="provinsi" class="form-control" v-model="provinsi">
        <option selected disabled value="">Pilih Provinsi</option>
        <option v-for="(item,i) in provOptionList" :key="i" :value="item.id"> {{item.name}}</option>
      </select>
    </section>
    <section>
      <label for="kota">Kota {{kota}}</label>
      <select name="" id="kota" class="form-control" v-model="kota">
        <option selected disabled value="">Pilih Kota</option>
        <option v-for="(item, index) in kotaOptionList" :key="index" :value="item.id" v-show="item.prov_id==provinsi">{{`${item.name} (${item.prov_id})`}}</option>
      </select>
    </section>
    <section class="mt-5">
      <form-select-option :optionList="provOptionList" placeholder="Pilih Provinsi" />
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selected: "",
      multiline: "",
      checked: true,
      checkedNames: [],
      provinsi: "",
      provOptionList: [
        { id: 1, name: "DKI Jakarta" },
        { id: 2, name: "Jawa Tengah" },
        { id: 3, name: "Jawa Timur" },
        { id: 4, name: "Jawa Barat" },
        { id: 5, name: "Kalimatan Selatan" },
        { id: 6, name: "Banten" },
      ],
      kota: "",
      kotaOptionList: [
        { id: 21, name: "Jakarta Barat", prov_id: 1 },
        { id: 22, name: "Sragen", prov_id: 2 },
        { id: 23, name: "Surabaya", prov_id: 3 },
        { id: 24, name: "Bandung", prov_id: 4 },
        { id: 25, name: "Bau-Bau", prov_id: 5 },
        { id: 26, name: "Tangerang", prov_id: 6 },
      ],
    };
  },
};
</script>