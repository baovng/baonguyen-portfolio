<template>
  <div class="container-fluid wrapper  my-5">
    <div class="d-flex align-items-start contact-wrapper flex-column justify-content-center mx-5">
      <div class="container mt-3 mb-5">
          <div class="header-4 mt-5 mb-4">Contact !</div>
        <div class="bh6 fw-bold"> Get In Touch</div>
        <div class="bh3 mt-2">{{messageContact}}</div>
        <a href="" target="_blank" rel="noopener noreferrer" class="btn btn-lg btn-custom mt-5 px-5 btn-nav">Say Hi</a>

      </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            messageContact:"I'm excited to take the next step in my career and am open to exploring new opportunities in my field.If you have any suggestions or job openings to share, please send me an email - I'd be grateful for any assistance!"
        }
    }

}
</script>

<style>
.contact-wrapper{
    width: 850px;
    max-width: 100%;
    height: 90vh;
}
.header-4{
    position: relative;
    font-size: 1.5rem;
    color: var(--primary-color);
    font-weight: 700;
    font-family: "Roboto";
}
.header-4::before {
  content: "04.  ";
  left: 0;
  font-size: 1.4rem;
  color: var(--primary-color);
}
.vh-80{
    height: 80vh;
}
</style>