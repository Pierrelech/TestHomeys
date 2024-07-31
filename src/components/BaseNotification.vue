<template>
	<main>
        <div class="notification">
            <div class="modal-header">
                <img src="../../icons/Danger.svg" alt="Danger Icon" />
                <h1>Modal Windows</h1>
                <button class="close-button">&times;</button>
            </div>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit ut aliquam, purus sit amet luctus venenatis, lectus magna fringilla urna, porttitor</p>
        </div>
	</main>
</template>

<script setup>
</script>

<style scoped>
.notification {
    width: 527px; 
    height: 160px; 
    top: 32px;
    left: 16px;
    padding: 24px;
    gap: 8px;
    border-radius: 16px;
    border: 2px solid #D29393; 
    opacity: 1; 
    background: #F7E4E4;
    box-shadow: 0px 6px 12px 0px #0000001A;
}

.modal-header {
    display: flex; 
    align-items: center; 
    width: 479px; 
    height: 32px; 
    gap: 16px;
    opacity: 1; 
}

h1 {
    width: 395px;
    height: 28px;
    gap: 0px;
    opacity: 1; 
    font-family: DM Sans;
    font-size: 20px;
    font-weight: 500;
    line-height: 28px;
}
.close-button {
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
}

p {
    width: 479px; 
    height: 72px; 
    padding: 0px 0px 0px 48px;
    gap: 0px;
    opacity: 1; 
}
</style>
