<template>
    <section>
        <header>
            <slot name="header"></slot>
        </header>
        <slot></slot>
    </section>
</template>

 <style scoped>
section {
  margin: 2rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
}
header {
    width: 100%;
    height: 5rem;
    display: flex;
   
    justify-content: space-between; 
    align-items: center;
    padding-right: 10px;
    background-color: #9a83da;
  }
  header h1 {
    color: rgb(14, 2, 2);
    margin: 0;
  }


 </style>