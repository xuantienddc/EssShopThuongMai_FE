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
            <li class="nav-item dropdown">
                <a href="javascript:;" class="nav-link dropdown-toggle dropdown-toggle-nocaret"
                    data-bs-toggle="dropdown">
                    <div class="parent-icon"><i class='bx bx-home-circle'></i>
                    </div>
                    <div class="menu-title">Dashboard</div>
                </a>
                <ul class="dropdown-menu">
                    <li> <a class="dropdown-item" href="index.html"><i
                                class="bx bx-right-arrow-alt"></i>Default</a>
                    </li>
                    <li> <a class="dropdown-item" href="index2.html"><i
                                class="bx bx-right-arrow-alt"></i>Alternate</a>
                    </li>
                    <li> <a class="dropdown-item" href="index3.html"><i
                                class="bx bx-right-arrow-alt"></i>Graphical</a>
                    </li>
                </ul>
            </li>
            <li class="nav-item">
                <router-link to="/admin/san-pham">
                    <a class="nav-link" href="/admin/san-pham">
                        <div class="parent-icon"><i class="fa-brands fa-product-hunt"></i>
                        </div>
                        <div class="menu-title">Sản Phẩm</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/nhan-vien">
                    <a class="nav-link" href="/admin/nhan-vien">
                        <div class="parent-icon"><i class="fa-solid fa-person"></i>
                        </div>
                        <div class="menu-title">Nhân Viên</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/dai-ly">
                    <a class="nav-link" href="/admin/dai-ly">
                        <div class="parent-icon"><i class="fa-solid fa-truck-field"></i>
                        </div>
                        <div class="menu-title">Đại Lý</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/danh-muc">
                    <a class="nav-link" href="/admin/danh-muc">
                        <div class="parent-icon"><i class="fa-solid fa-list"></i>
                        </div>
                        <div class="menu-title">Danh Mục</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/phan-quyen">
                    <a class="nav-link" href="/admin/phan-quyen">
                        <div class="parent-icon"><i class="fa-solid fa-list"></i>
                        </div>
                        <div class="menu-title">Phân Quyền</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/phieu-khuyen-mai">
                    <a class="nav-link" href="/admin/phieu-khuyen-mai">
                        <div class="parent-icon"><i class="fa-solid fa-tags"></i>
                        </div>
                        <div class="menu-title">Phiếu Khuyến Mãi</div>
                    </a>
                </router-link>
            </li>
            <li class="nav-item">
                <router-link to="/admin/quan-ly-don-hang">
                    <a class="nav-link" href="/admin/quan-ly-don-hang">
                        <div class="parent-icon"><i class="fa-brands fa-first-order-alt"></i>
                        </div>
                        <div class="menu-title">Đơn Hàng</div>
                    </a>
                </router-link>
            </li>
        </ul>
    </nav>
</div>
</template>
<script>
export default {
    
}
</script>
<style>
    
</style>