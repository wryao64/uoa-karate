<template>
  <div>
    <h1>A collection of useful forms and websites</h1>
    <div class="container">
      <ul>
        <li>
          <router-link :to="'/grading-info/'">
            What do I need to know to grade?
          </router-link>
        </li>
        <li>
          <a
            href="https://www.youtube.com/playlist?list=PLjmMUBeoZL9eM-TUV8YFDd0w0IIfQ2lLc"
            target="_blank"
          >Club Video Playlist</a>
        </li>
        <li>
          <a
            href="https://goo.gl/forms/YMUAxBg9q3fgG0VB3"
            target="_blank"
          >Club Reimbursement Form</a>
        </li>
        <li><a
            href="https://goo.gl/forms/sTq5WHgxXTOSmMx42"
            target="_blank"
          >Club Sign Up Sheet</a></li>
        <li><a
            href="http://karate.org.nz/"
            target="_blank"
          >IOGKFNZ's Website</a></li>
        <li><a
            href="https://drive.google.com/file/d/1ej27e0nkSEZgCooaJor7WsK9nIFzJx7Y/view?usp=sharing"
            target="_blank"
          >Health and Safety Guidelines</a></li>
        <li><a
            href="https://drive.google.com/open?id=0B-VdjkUccnFtQUIxM0tJUnNvSzg"
            target="_blank"
          >Beginner's Guide to Goju Ryu</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "LinkDirectory",
  components: {}
};
</script>

<style scoped>
.container {
  text-align: left;
  display: grid;
  align-items: center;
  justify-items: center;
  grid-template-columns: repeat(2, minmax(300px, 1fr));
}

.container p {
  max-width: 600px;
  align-self: flex-start;
}

h1 {
  text-align: center;
}
</style>

