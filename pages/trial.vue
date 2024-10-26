<template>
    <div class="talent-container">
        <div class="search-bar">
            <input type="text" v-model="searchQuery" placeholder="Ketik di sini yaa" class="search-input"/>
        </div>
      <div class="talent-grid">
        <div
          class="talent-card"
          v-for="talent in filteredTalents"
          :key="talent.id">
          <div class="talent-info">
            <h2 class="talent-name">{{ talent.name }}</h2>
            <p class="talent-location">Lokasi: {{ talent.location }}</p>
            <p class="talent-age">Umur: {{ talent.age }} tahun</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        searchQuery: '',
        talents: [
          { id: 1, name: 'Nova Sinclair', location: 'Jakarta', age: 21 },
          { id: 2, name: 'Jasmine Carter', location: 'Los Angeles', age: 39 },
          { id: 3, name: 'Luna Evans', location: 'Washington, D.C.', age: 27 },
          { id: 4, name: 'Mila Hawthorne', location: 'London', age: 29 },
          { id: 5, name: 'Aria James', location: 'Boca Raton, Florida', age: 31 },
          { id: 6, name: 'Zara Taylor', location: 'Bali', age: 25 },
          { id: 7, name: 'James Smith', location: 'Jakarta', age: 25 },
          { id: 8, name: 'Sophia Turner', location: 'Yogyakarta', age: 29 },
          { id: 9, name: 'Lucas Adams', location: 'Bandung', age: 32 },
          { id: 10, name: 'Emily Brown', location: 'Surabaya', age: 30 },
          { id: 11, name: 'Ethan White', location: 'Jakarta', age: 27 },
          { id: 12, name: 'Grace Martin', location: 'Bali', age: 33 },
          { id: 13, name: 'Henry Moore', location: 'Surabaya',  age: 33 },
          { id: 14, name: 'Zoe Johnson', location: 'Jakarta',  age: 29 },
          { id: 15, name: 'Benjamin Wilson', location: 'Yogyakarta', age: 27 },
          { id: 16, name: 'Chloe Harris', location: 'Jakarta',  age: 26 },
          { id: 17, name: 'Mason Lee', location: 'Bali', age: 30 },
          { id: 18, name: 'Isabella Clark', location: 'Surabaya', age: 24 },
          { id: 19, name: 'Michael Thompson', location: 'Bandung', age: 30 },
          { id: 20, name: 'Lily Martinez', location: 'Jakarta', age: 25 },
          { id: 21, name: 'Sophie Robinson', location: 'Surabaya', age: 32 },
          { id: 22, name: 'Oliver Nelson', location: 'Yogyakarta', age: 33 },
          { id: 23, name: 'Ella King', location: 'Bali', age: 34, },
          { id: 24, name: 'Daniel Walker', location: 'Jakarta', age: 34 },
          { id: 25, name: 'Ava Wright', location: 'Surabaya', age: 30 },
          { id: 26, name: 'Chania Azzahra', location: 'Malang', age: 24 },
        ],
      };
    },
    computed: {
      filteredTalents() {
        return this.talents.filter(talent =>
          talent.name.toLowerCase().includes(this.searchQuery.toLowerCase())
        );
      },
    },
  };
  </script>
  
  <style scoped>

  .search-bar{
    padding: 30px;
    background-color: #1a1a1a;
    display: flex;
    flex-direction: column;
    align-items: center; 
  }
  
  .talent-container {
    padding: 30px;
    background-color: #1a1a1a;
    min-height: 100vh;
  }
  
  .title {
    text-align: center;
    font-size: 28px;
    margin-bottom: 20px;
    color: #ffffff; 
  }
  
  .search-input {
    width: 500px;
    padding: 9px;
    margin-bottom: 20px;
    border: 1px solid #ddd;
    border-radius: 20px;
    font-size: 16px;
    transition: border-color 0.3s;
  }
  
  .search-input:focus {
    border-color: blue;
    outline: none;
  }
  
  .talent-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 30px;
  }
  
  .talent-card {
    background-color: #ffffff;
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s;
  }
  
  .talent-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
  }

  
  .talent-info {
    margin-top: 15px;
  }
  
  .talent-name {
    font-size: 20px;
    margin: 10px 0;
    color: blue;
    font-weight: bolder;
  }
  
  .talent-location,
  .talent-age {
    font-size: 14px;
    margin: 5px 0;
    color: #3a3737;
  }
  


  </style> 
  