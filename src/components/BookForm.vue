<template>
    <form class="" action="#" method="post">
        <input type="text" name="title" value="" placeholder="Book Title">
        <input type="text" name="author" value="" placeholder="Book Author">
        <button type="submit" name="button" @click.prevent="bookSubmit">Add Book</button>
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