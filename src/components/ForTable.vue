<template>
    <div class="row">
        <div class="col-12">
            <div class="card  shadow-lg p-3 mb-5 bg-body rounded">
                <div class="card-header mt-2">
                    <div class="row">
                        <div class="col-6">
                            <h5>Danh Sách Sản Phẩm</h5>
                        </div>
                        <div class="col-6">
                            <button class="btn btn-outline-primary float-end" data-bs-toggle="modal"
                                data-bs-target="#themmoimodal">Thêm mới</button>
                        </div>
                    </div>
                </div>
                <div class="card-body">
                    <div class="table-responsive">
                        <table class="table table-bordered table-hover">
                            <thead>
                                <tr class="text-center align-middle">
                                    <th>#</th>
                                    <th>Tên Sản Phẩm</th>
                                    <th>Hình Ảnh</th>
                                    <th>Mô tả</th>
                                    <th>Số Lượng Nhập</th>
                                    <th>Giá Bán</th>
                                    <th>Giá Khuyến Mãi</th>
                                    <th>Tình trạng</th>
                                    <th>Action</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr v-for="(v, k) in list_san_pham">
                                    <th class="align-middle text-nowrap text-center">{{ k + 1 }}</th>
                                    <td class="align-middle text-nowrap">{{ v.ten_san_pham }}</td>
                                    <td class="align-middle text-center">
                                        <img :src="v.hinh_anh" class="img-fluid" style="height: 100px; width: 100%;" alt="">
                                    </td>
                                    <td class="align-middle text-nowrap">{{ v.mo_ta_ngan }}</td>
                                    <td class="align-middle text-nowrap text-center">{{ v.so_luong_nhap }}</td>
                                    <td class="align-middle text-nowrap text-end">{{ v.gia_ban }} đ</td>
                                    <td class="align-middle text-nowrap text-end">{{ v.gia_khuyen_mai }} đ</td>
                                    <td class="align-middle text-nowrap text-center">
                                        <button v-if="v.tinh_trang == 1" class="btn btn-success">Hoạt Động</button>
                                        <button v-else class="btn btn-warning">Tạm Dừng</button>
                                    </td>
                                    <td class="align-middle text-nowrap text-center">
                                        <button class="btn btn-primary" data-bs-toggle="modal"
                                            data-bs-target="#capNhatmodal">Cập Nhật</button>
                                        <button class="btn btn-danger" data-bs-toggle="modal"
                                            data-bs-target="#xoaModal">Xóa</button>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
        <div class="modal fade" id="themmoimodal" tabindex="-1" aria-labelledby="exampleModalLabel"
            aria-hidden="true">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">Thêm Mới</h1>
                        <button type="button" class="btn-close" data-bs-dismiss="modal"
                            aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-6 mb-2">
                                <label class="form-label">Tên Sản Phẩm</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Hình Ảnh</label>
                                <input type="email" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Mô tả</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Số Lượng Nhập</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Giá Bán</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Giá Khuyến Mãi</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Tình trạng</label>
                                <select class="form-select">
                                    <option value="0">Tạm tắt</option>
                                    <option value="1">Hiển thị</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary"
                            data-bs-dismiss="modal">Close</button>
                        <button data-bs-dismiss="modal" type="button" class="btn btn-primary">Xác nhận</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="modal fade" id="capNhatmodal" tabindex="-1" aria-labelledby="exampleModalLabel"
            aria-hidden="true">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">Cập Nhật</h1>
                        <button type="button" class="btn-close" data-bs-dismiss="modal"
                            aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-6 mb-2">
                                <label class="form-label">Tên Sản Phẩm</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Hình Ảnh</label>
                                <input type="email" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Mô tả</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Số Lượng Nhập</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Giá Bán</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Giá Khuyến Mãi</label>
                                <input type="text" class="form-control">
                            </div>
                            <div class="col-6 mb-2">
                                <label class="form-label">Tình trạng</label>
                                <select class="form-select">
                                    <option value="0">Tạm tắt</option>
                                    <option value="1">Hiển thị</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary"
                            data-bs-dismiss="modal">Close</button>
                        <button data-bs-dismiss="modal" type="button" class="btn btn-primary">Xác
                            nhận</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="modal fade" id="xoaModal" tabindex="-1" aria-labelledby="exampleModalLabel"
            aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">Xóa</h1>
                        <button type="button" class="btn-close" data-bs-dismiss="modal"
                            aria-label="Close"></button>
                    </div>
                    <div class="modal-body">
                        <div
                            class="alert alert-warning border-0 bg-warning alert-dismissible fade show py-2">
                            <div class="d-flex align-items-center">
                                <div class="font-35 text-dark"><i class="bx bx-info-circle"></i>
                                </div>
                                <div class="ms-3">
                                    <h6 class="mb-0 text-dark">Warning</h6>
                                    <div class="text-dark">
                                        <p>Bạn có muốn xóa sản phẩm <b>XXX</b> này không?
                                        </p>
                                        <p>
                                            <b>Lưu ý:</b> Điều này không thể hoàn tác!
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary"
                            data-bs-dismiss="modal">Close</button>
                        <button type="button" class="btn btn-danger">Xóa</button>
                    </div>
                </div>
            </div>
        </div>
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
    <style>
        
    </style>