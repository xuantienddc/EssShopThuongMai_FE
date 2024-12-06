<template>
    <div class="row">
        <div class="col-12">
            <div class="card">
                <div class="card-body">
                    <label class="form-label">Chọn </label>
                    <select class="form-select"  >
                        <template v-for="(v, k) in list_game">
                            <option :value="v.id">
                                {{ v.ten_san_pham }}
                            </option>
                        </template>
                        
                    </select>
                </div>
            </div>
        </div>
        <!-- <template v-for="(v, k) in list_nhac">
            <div class="col-4">
                <div class="card mb-3" style="max-width: 540px;">
                    <div class="row g-0">
                        <div class="col-md-4">
                            <img :src="v.hinh_anh" style="height: 150px;" class="img-fluid rounded-start" alt="...">
                        </div>
                        <div class="col-md-8">
                            <div class="card-body">
                                <h5 class="card-title">{{ v.ten_bai_hat }}</h5>
                                <p class="card-text">{{ v.ca_si }}</p>
                                <p class="card-text"><small class="text-body-secondary">{{ v.thoi_gian }}</small></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </template> -->
    </div>
</template>
<script>
import axios from 'axios';
export default {
    data() {
        return {
            list_game: [],
        }
    },
    mounted() {
        this.loadDataGame();
    },
    methods: {
        loadDataGame() {
            axios
                .get('https://osm.dzfullstack.com/api/san-pham/data')
                .then((res) => {
                    this.list_game = res.data.data;
                });
        },

    }
}
</script>
<style></style>