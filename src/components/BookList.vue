<template>
<div>
    <h1>{{title}}</h1>
    <ol>
        <li v-for="book in books" :key="book.title">
            {{book.title}} {{book.author}}
        </li>
    </ol>
</div>
</template>

<script>
export default {
    name: "BookList",
    data: {
        title: "All Books",
        books: [
                {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
                {title: 'American Gods', author: 'Neil Gaiman'},
                {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
                ]
    }
}
</script>

<style>
    h1, h2 {
        font-weight: normal;
    }
    ol {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: block;
        margin: 0 10px;
    }

</style>
