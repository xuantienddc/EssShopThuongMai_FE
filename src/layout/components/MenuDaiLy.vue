<template>
    <div class="nav-container primary-menu">
        <div class="mobile-topbar-header">
            <div>
                <img src="../../assets/images/logo-icon.png" class="logo-icon" alt="logo icon">
            </div>
            <div>
                <h4 class="logo-text">Rukada</h4>
            </div>
            <div class="toggle-icon ms-auto"><i class='bx bx-arrow-to-left'></i>
            </div>
        </div>
        <nav class="navbar navbar-expand-xl w-100">
            <ul class="navbar-nav justify-content-start flex-grow-1 gap-1">
                <li class="nav-item">
                    <router-link to="/dai-ly/san-pham">
                        <a class="nav-link" href="/dai-ly/san-pham">
                            <div class="parent-icon"><i class="fa-brands fa-product-hunt"></i>
                            </div>
                            <div class="menu-title">Sản Phẩm</div>
                        </a>
                    </router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/dai-ly/nhap-kho">
                        <a class="nav-link" href="/dai-ly/nhap-kho">
                            <div class="parent-icon"><i class="fa-solid fa-person"></i>
                            </div>
                            <div class="menu-title">Nhập Kho</div>
                        </a>
                    </router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/dai-ly/danh-sach-nhap-kho">
                        <a class="nav-link" href="/dai-ly/danh-sach-nhap-kho">
                            <div class="parent-icon"><i class="fa-solid fa-bars"></i>
                            </div>
                            <div class="menu-title">Danh Sách Nhập Kho</div>
                        </a>
                    </router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/dai-ly/thong-ke-kho">
                        <a class="nav-link" href="/dai-ly/thong-ke-kho">
                            <div class="parent-icon"><i class="fa-solid fa-square-poll-vertical"></i>
                            </div>
                            <div class="menu-title">Thống Kê Nhập Kho</div>
                        </a>
                    </router-link>
                </li>
                <li class="nav-item dropdown">
                    <a href="javascript:;" class="nav-link dropdown-toggle dropdown-toggle-nocaret"
                        data-bs-toggle="dropdown">
                        <div class="parent-icon"><i class="fa-solid fa-magnifying-glass-chart"></i>
                        </div>
                        <div class="menu-title">Thống Kê</div>
                    </a>
                    <ul class="dropdown-menu">
                        <li> 
                            <router-link to="/dai-ly/thong-ke-1">
                                <a class="dropdown-item" href="index.html"><i class="fa-solid fa-chart-pie"></i>Thống Kê Số Lượng</a>
                            </router-link>
                        </li>
                        <li> 
                            <router-link to="/dai-ly/thong-ke-2">
                                <a class="dropdown-item" href="index2.html"><i class="fa-solid fa-chart-simple"></i>Thống Kê Số Tiền</a>
                            </router-link>
                        </li>
                    </ul>
                </li>
            </ul>
        </nav>
    </div>
</template>
<script>
export default {

}
</script>
<style></style>