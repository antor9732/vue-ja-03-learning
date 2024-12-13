<template>
    <header>
        <h1>MAHMUDUL</h1>
        <nav>
            <a href="#">HOME</a>
            <a href="#">ABOUT</a>
            <a href="#">PROJECTS</a>
            <a href="#">CONTACTS</a>
            <a href="#">CAREER</a>
        </nav>
    </header>
</template>

<style scoped>
h1{
    text-decoration: underline;
    color: aliceblue;
}
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    margin: 0px;
    background-color: royalblue;
}
header nav{
   display: flex;
   align-items: center;
   gap: 10px;
}
header nav a{
   color: black;
    text-decoration: none;
}
header nav a:hover {
   color: white;
    text-decoration: none;
}
</style>