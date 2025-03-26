<script>
Import ChildComponent from "./components/ChildComponent.vue"; // Impor komponen yang benar

export default (
  components: {
    ChildComponent,
  },
  data() {
    return {
      message: "",
      datalist: [],
      loading: false,
    };
  },
  methods: {
    
    handleCallback(data) {
    this.message = data;
    console.log("Callback diterima: ${data}");
  },
  
  
  fetchData() {
    return new Promise((resolve, reject) => (
      setTimeout(() » {
        const success = true;
        if (success) {
          resolve(["Data 1", "Data 2", "Data 3"]);
        } else {
          reject("Gagal mengambil data!");
        }
      ), 2000);
    });
  },

  Codeium: Refactor|Explain|X
  loadData() {
    this.loading true;
    this.fetchData()
      .then((data) => {
        this.datalist =data;
        console.log("Data berhasil diambil:", data);
      })
      .catch((error) => {
        console.error(error);
      })
      .finally (() => {
        this.loading = false;
      }
    },

    Codeium: Refactor|Explain|X
    async loadDataAsync() {
      this.loading {true;
      try {
        this.datalist await this.fetchData();
        console.log("Data berhasil diambil (Async/Await):", this.dataList);
      } catch (error) {
        console.error(error);
      } finally {
        this.loading - false;
      }
    },

    Codelum: Refactor | Explain (X
    handleItemClick(item) {
      console.log("Berhasil masuk ke ${item)");
      alert("Berhasil masuk ke $(item)); // Menampilkan alert juga
    },
  },
};
</script>
