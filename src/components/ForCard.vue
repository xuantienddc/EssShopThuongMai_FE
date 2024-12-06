<template>
    <div class="row row-cols-1 row-cols-sm-2 row-cols-lg-4 row-cols-xl-4 row-cols-xxl-4 product-grid">
        <template v-for="(v, k) in list_san_pham">
            <div class="col d-flex align-items-stretch">
                <div class="card">
                    <img :src="v.hinh_anh" class="card-img-top" alt="...">
                    <div class="">
                        <div class="position-absolute top-0 end-0 m-3 product-discount"><span class="">-10%</span></div>
                    </div>
                    <div class="card-body">
                        <h6 class="card-title cursor-pointer">{{ v.ten_san_pham }}</h6>
                        <div class="clearfix">
                            <p class="mb-0 float-start"><strong>{{ v.so_luong_nhap }}</strong> Sales</p>
                            <p class="mb-0 float-end fw-bold"><span class="me-2 text-decoration-line-through text-secondary">{{ v.gia_ban }}đ</span><span>{{ v.gia_khuyen_mai }}đ</span></p>
                        </div>
                        <div class="d-flex align-items-center mt-3 fs-6">
                            <div class="cursor-pointer">
                            <i class='bx bxs-star text-warning'></i>
                            <i class='bx bxs-star text-warning'></i>
                            <i class='bx bxs-star text-warning'></i>
                            <i class='bx bxs-star text-warning'></i>
                            <i class='bx bxs-star text-secondary'></i>
                            </div>	
                            <p class="mb-0 ms-auto">4.2(182)</p>
                        </div>
                    </div>
                </div>
            </div>
        </template>
    </div>
</template>
<script>
import axios from 'axios';
export default {
    data() {
        return {
            list_san_pham   :   [],
        }
    },
    mounted() {
        this.loadDataSanPham();
    },
    methods: {
        loadDataSanPham()   {
            axios
                .get('https://osm.dzfullstack.com/api/san-pham/data')
                .then((res) =>  {
                    this.list_san_pham = res.data.data;
                });
        },

    }
}
</script>
<style></style>