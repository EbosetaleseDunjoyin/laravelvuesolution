<template>
  <div id="main" class="">
    <div class="container-fluid record-screen ">
      <div class="row d-flex justify-content-center">
        <div class=" top-record-text">
          <p class=""><i class="bi bi-record2"></i>Live Preview</p>
        </div>
        <video id="square" class="square mb-5"></video>
        <div class="d-flex justify-content-center  ">
          <button type="submit" id="stopRec" class="primary-btn  "
            style="padding:13px 75px ;  font: normal normal normal 18px/27px Poppins;" disabled='disabled'>Stop
            Recording</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      audioget: null,
      screenget: null,
      videoget: null
    }
  },
  mounted: async function () {
    // const data = []
    this.audioget = this.$route.params.audios
    this.screenget = this.$route.params.streams
    this.videoget = this.$route.params.videos
    console.log(this.screenget)
    if (this.screenget === 'true') {
      // let streamed = null
      this.videoget = false
      const stream = await navigator.mediaDevices.getDisplayMedia({
        video: { mediaSource: 'screen' }
      })
      if (stream) {
        const video = document.querySelector('.square')
        video.srcObject = stream
        video.play()
      } else {
        console.warn('No stream available')
      }
      // const mediarecord = new MediaRecorder(stream)
      // mediarecord.ondataavailable = (e) => {
      //   data.push(e.data)
      // }
      // mediarecord.start = (e) => {
      //   document.querySelector('#square').src = URL.createObjectURL(
      //     new Blob(data, {
      //       type: data[0].type
      //     })
      //   )
      // }
      console.log(stream)
    }
  }
}
</script>
