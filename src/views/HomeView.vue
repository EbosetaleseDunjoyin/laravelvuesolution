<template>
  <!-- main section -->
  <div id="main">
    <div class="container-fluid">
      <div class="row">
        <div class="col-2">
          <div id="sidebar">
            <ul class="menu">
              <li class="sidebar-item active mb-4">
                <a href="index.html" class='sidebar-link'>
                  <i class="bi bi-film px-3"></i>
                  <span>My Recordings</span>
                </a>
              </li>
              <li class="sidebar-item  mb-4">
                <a href="index.html" class='sidebar-link'>
                  <i class="bi bi-share px-3"></i>
                  <span>Requested</span>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-10">
          <div class="container-fluid main-content">
            <div class="row mt-5">
              <div class="col-4">
                <div class="bread_crumbs">
                  <nav style="--bs-breadcrumb-divider: '>';" aria-label="breadcrumb">
                    <ol class="breadcrumb">
                      <li class="breadcrumb-item"><a href="#">Snapbyte</a></li>
                      <li class="breadcrumb-item active" aria-current="page">My Recordings</li>
                    </ol>
                  </nav>
                </div>
                <div class="bread_crumbs_title">
                  <h4>My Recordings <span class="bread_crumbs_title_number">25</span> </h4>
                </div>
              </div>
              <div class="col-8 ">
                <div class="bread-crumb-buttons pt-4 d-flex justify-content-lg-center ">
                  <button class="primary-alt mx-2"><i class="bi bi-arrow-down-up px-2"></i>By Date</button>
                  <button class="primary-alt mx-2"><i class="bi bi-funnel px-2"></i>Add Filter <i
                      class="bi bi-chevron-down px-1"></i></button>
                  <button class="primary-btn mx-2"><i class="bi bi-camera-video px-2"></i>New Request</button>
                  <button class="secondary-btn mx-2" data-bs-toggle="modal" data-bs-target="#recordModal"><i
                      class="bi bi-record-circle px-2"></i>Start Recording</button>
                </div>
              </div>
            </div>
          </div>
          <div class="container-fluid main-content">
            <div class="row mt-5 ">
              <table class="table table-borderless">
                <thead class="mb-3">
                  <tr>
                    <th scope="col">Recordings</th>
                    <th scope="col">Title</th>
                    <th scope="col">Views</th>
                    <th scope="col">Size</th>
                    <th scope="col">Last Modified</th>
                    <th scope="col"></th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>
                      <div class="table-img">
                        <img src="../assets/assets/2.jpg" class="img-fluid" alt="">
                        <div class="table-no">
                          <p>00:14</p>
                        </div>
                      </div>
                    </td>
                    <td>
                      <div class="table-title">
                        <h6>Getting it right the first time</h6>
                        <p>
                          The Video description is shown here if the user has added it.
                        </p>
                      </div>
                    </td>
                    <td>324</td>
                    <td>923 KB</td>
                    <td>3 months ago</td>
                    <td>
                      <i class="bi bi-three-dots"></i>
                    </td>
                  </tr>
                  <tr>
                    <td>
                      <div class="table-img">
                        <img src="../assets/assets/3.jpg" class="img-fluid" alt="">
                        <div class="table-no">
                          <p>00:14</p>
                        </div>
                      </div>
                    </td>
                    <td>
                      <div class="table-title">
                        <h6>Getting it right the first time</h6>
                        <p>
                          The Video description is shown here if the user has added it.
                        </p>
                      </div>
                    </td>
                    <td>324</td>
                    <td>923 KB</td>
                    <td>3 months ago</td>
                    <td>
                      <i class="bi bi-three-dots"></i>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid">
      <div class="modal fade "  id="recordModal" tabindex="-1"
        aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog ">
          <div class="modal-content ">
            <div class="modal-header">
              <h5 class="modal-title" id="exampleModalLabel">New Recording</h5>
              <button type="button" class="btn-close " data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
              <form @submit.prevent="recordSubmit">
                <p>Save the recording in</p>
                <select class="form-select mb-5" aria-label="Default select example">
                  <option selected>Select a project</option>
                  <option value="1">Nothing here</option>
                </select>

                <div class="check-boxe  mb-3">

                  <div class="row">
                    <div class="col-10">
                      <h6 class="">Record Screen </h6>

                    </div>
                    <div class="col-2 d-flex justify-content-end">
                      <div class="form-check  form-switch">
                        <input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckChecked"
                          @change="screenallow = !screenallow">
                      </div>
                    </div>
                  </div>
                </div>
                <div class="check-boxe  mb-3">
                  <div class="row">
                    <div class="col-10">
                      <h6 class="">Record Camera</h6>
                    </div>
                    <div class="col-2 d-flex justify-content-end">
                      <div class="form-check  form-switch">
                        <input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckChecked"
                          @change="videoallow = !videoallow">
                      </div>
                    </div>
                  </div>
                </div>
                <div class="check-boxe  mb-3">
                  <div class="row">
                    <div class="col-10">
                      <h6 class="">Record Mic</h6>
                    </div>
                    <div class="col-2 d-flex justify-content-end">
                      <div class="form-check  form-switch">
                        <input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckChecked"
                          @change="micallow = !micallow">
                      </div>
                    </div>
                  </div>
                </div>
                <div class="d-flex justify-content-center">
                  <button type="submit" class="primary-btn  mx-2"
                    style="padding:13px 75px ; font: normal normal normal 18px/27px Poppins;">Start Recording</button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- main section -->
</template>

<script>
// @ is an alias to /src
export default {
  data () {
    return {
      message: 'Hello Vue!',
      savehere: '',
      screenallow: false,
      cameraallow: false,
      micallow: false,
      stream: null,
      audio: null,
      video: null,
      mixedStream: null,
      chunks: [],
      recorder: null,
      startButton: null,
      stopButton: null,
      downloadButton: null,
      recordedVideo: null
    }
  },
  methods: {
    check (e) {
      console.log(e.target.checked, this.screenallow)
    },
    async recordSubmit () {
      this.$router.push({
        name: 'record',
        params: {
          audios: this.audio,
          streams: this.screenallow,
          // streams: [this.stream],
          videos: this.video
        }
      })
      if (this.micallow) {
        await navigator.mediaDevices.getUserMedia({
          audio: {
            echoCancellation: true,
            noiseSuppression: true,
            sampleRate: 44100
          }
        })
      }
      if (this.cameraallow) {
        this.screenallow = false
        this.video = await navigator.mediaDevices.getUserMedia({
          video: true,
          audio: true
        }).then(vidStream => {
          document.querySelector('.square').src = vidStream
        })
      }
      document.querySelector('.modal-backdrop.fade').style.display = 'none'
    },
    allowscreen () {
      return navigator.mediaDevices.getDisplayMedia({
        video: { mediaSource: 'screen' }
      })
    }
  }
}
</script>
