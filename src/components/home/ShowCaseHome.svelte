

<script>
    import playButton from "../../assets/images/icons/play-button.png"

</script>

<section class="homecontainer">
    <div class="homecontainerback"></div>
    <div class="homecontaineroverlay"></div>
    <div class="homecontainercontents">
        <h2>Captain Marvel</h2>
        <h4>
            Now on Blu-ray
            <sup class="homecontainersup">TM</sup>,4K Ultra
            HD<sup class="homecontainersup">TM</sup> and
            Digital
          </h4>
          <div class="previewcontainer">
            <a
              href="https://www.imdb.com/title/tt4154664/"
              target="_blank"
              rel="noreferrer"
              class="previewbutton"
            >
              <img src={playButton} alt="Playbutton">
              <small>Preview</small>
            </a>
          </div>
    </div>
</section>


<style lang="scss">
    .homecontainer {
  width: 100vw;
  height: 100vh;

  .homecontainerback {
    width: 100vw;
    height: 100vh;
    position: absolute;
    background: url("../../assets/images/captain-marvel.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
  }
  .homecontaineroverlay {
    width: 100vw;
    height: 100vh;
    position: absolute;
    background: rgba(0, 0, 0, 0.598);
  }
  .homecontainercontents {
    position: relative;
    z-index: 2;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    padding-top: 330px;
    h2 {
      font-size: 50px;
      color: #fff;
    }
    h4 {
      color: #fff;
      .homecontainersup {
        font-size: 10px;
      }
    }
    .previewcontainer {
      background-color: none;
      a {
        display: flex;
        border: solid 3px #fff;
        gap: 1rem;
        border-radius: 24px;
        cursor: pointer;
        padding-left: 50px;
        padding-right: 50px;
        padding-top: 10px;
        padding-bottom: 10px;
        color: #fff !important;
        font-size: 20px;
        &:hover {
          background-color: rgba(255, 255, 255, 0.26);
          color: #fff;
        }
        img{
            width: 30px;
            height: 30px;
        }
      }
    }
  }
}

</style>