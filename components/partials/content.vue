<template>
   <div class="container">
            <div class="row justify-content-center">
                <div class="col-sm-3">
                    <div class="card text-white bg-primary mb-3 text-center">
                        <div class="card-body">
                            <h6 class="card-title text-left">Homework Mendatang</h6>
                            <p class="card-text text-left">Batas Waktu Pengumpulan Hari Ini:</p>
                            <p class="card-text text-center">
                                23:59 Homework Front End
                            </p>
                        </div>
                    </div>
                </div>

                <div class="col-sm-9">
                    <form>
                        <div class="form-group">
                            <textarea name="message" id="message" class="form-control" placeholder="Masukan Komenter Anda dikelas ini"></textarea>
                        </div>
                        <div class="form-group">
                            <button type="submit" class="btn btn-info">Kirim Pesan!</button>
                        </div>
                        <div class="card bg-dark text-white">
                            <img src="~/assets/img/pc_gaming.jpg" style="height: 280px" class="card-img">
                            <div class="card-img-overlay">
                                <h5 class="card-title">SPV class memposting materi terbaru: Sesion 1</h5>
                                <p class="card-text">14 April 2021</p>
                            </div>
                        </div>
                        <div class="card bg-dark text-white">
                            <img src="~/assets/img/pc_gaming.jpg" style="height: 280px" class="card-img">
                            <div class="card-img-overlay">
                                <h5 class="card-title">SPV class memposting materi terbaru: Sesion 2</h5>
                                <p class="card-text">16 April 2021</p>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
          </div>
</template>