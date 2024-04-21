<template>
    <div class="skillscontainer mt-6">
        <div class="flex items-center my-4">
            <h1 class="text-3xl mr-2">My Skills</h1>
            <img src="../assets/pocion.png" alt="potion" class="potionimg">
        </div>
        <!-- <span>Tecnical skills learned so far:</span> -->
    </div>
    
</template>

<script setup>
</script>

<style scoped>
.skillscontainer {
    margin-left: 7rem; 
    padding-left: 0; 
    margin-top: 5rem;
}

.potionimg {
    width: 65px;
    height: 90px;
}

h1 {
    color: var(--stress-color);
    margin-left: 0; /* Alinea el h1 al margen izquierdo */
}

/* Alinea la imagen al margen izquierdo */
img {
    margin-left: 0;
}
</style>
