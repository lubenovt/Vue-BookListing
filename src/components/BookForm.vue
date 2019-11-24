<template>
    <form class="" action="#" method="post">
        <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
        <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
        <button name="button" v-on:submit.prevent="bookSubmit">Add Book</button>
    </form>
</template>

<script>
export default {
    name: "BookForm",
    props: [
        'books'
    ],
    data() {
        return {
            bookTitle: '',
            bookAuthor: ''
        }
    },
    methods: {
        bookSubmit: function(bookAuthor, bookTitle) {
            this.bookTitle = bookTitle;
            this.bookAuthor = bookAuthor;
        }
    }
}
</script>

<style>

</style>