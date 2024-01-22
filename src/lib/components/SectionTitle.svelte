<script>
    export let title = 'Default Title';
  </script>
  
  <div class="section-title">
    <i class="fa-solid fa-square"></i>
    <p class="title">{title}</p>
  </div>
  
  <style>
    .section-title {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 0;
      padding: 0;
      margin-bottom: 15px;
    }

    .section-title i {
    color: #509A23; 
    font-size: 0.7rem;
    }

    .title {
        font-weight: 500;
        font-size: 1.05rem;
        margin: 0;
        padding: 0;
    }
  </style>
  