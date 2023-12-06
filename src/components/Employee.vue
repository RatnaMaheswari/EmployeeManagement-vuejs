<script setup>
    defineProps(['employee'])
</script>
<template>
            <div class="employee-container">
                    <section class="profile">
                    <div class="profile-img">
                        <img :src="employee.image" alt="">
                    </div>

                    <div class="profile-desc">
                        <p class="name">{{ employee.employee_name }}</p>
                        <p class="role">{{ employee.role }}</p>
                        <p class="dept">{{ employee.department }} | {{ employee.location.city }}</p>
                    </div>
                </section>

        <section class="doj">
            <p ><span><i class="fa fa-sign-in" aria-hidden="true"></i></span>{{ employee.date_of_joining }}</p>
            <p ><span><i class="fa fa-user" aria-hidden="true"></i></span>{{ employee.reporting_to }}</p>
        </section>

        <section class="address">
            <p><span><i class="fa fa-usd" aria-hidden="true"></i></span>{{ employee.salary }}</p>
        </section>

                <section class="contact">
                    <p class="email"> <span><i class="fa fa-envelope" aria-hidden="true"></i></span> {{ employee.email }}</p>
                    <p class="phone"><span><i class="fa fa-phone" aria-hidden="true"></i></span> {{ employee.contact_number }}</p>
                    <p class="location"> <span><i class="fa fa-map-marker" aria-hidden="true"></i></span> 
                        {{employee.location.state }}, {{ employee.location.zip }}</p>
                </section>
                <section class="action">
                    <button  class="profile-btn">View Profile</button>
                </section>
            </div>
</template>
<style scoped>
.profile-btn {
    border: unset;
    background-color: #000;
    color: #fff;
    padding: 10px;
    font-weight: bold;
    border-radius: 10px;
    letter-spacing: 1px;
    cursor: pointer;
}
    article{
        padding: 15px;
    }
    span{
    padding-right: 10px
}
hr {
    width: 90%;
    margin: auto;
}
.employee-details {
    width: 30%;
    padding: 15px;
}
.employee-details p {
    text-align: center;
}
.employee-details article {
    box-shadow: rgba(14, 30, 37, 0.12) 0px 2px 4px 0px, rgba(14, 30, 37, 0.32) 0px 2px 16px 0px;
}
h3 {
    text-align: center;
    font-weight: bold;
    margin: 10px 0 20px 0;
}
    .employee-container {
        justify-content: space-between;
    display: flex;
    align-items: center;
    padding: 15px;
    }
    .profile{
        display: flex;
    grid-gap: 10px;
    align-items: center;
    }
    .profile-img, .profile-img img {
        width: 50px;
    height: 50px;
    border-radius: 50%;
    }
    .name {
        font-weight: bold;
    font-size: 16px;
    letter-spacing: 1px;
    color: #000;
    }
    .role, .dept{
        font-size: 13px;
    }
    p{
        line-height: 25px;
        color: #625e5e;
        font-size: 13px;
    }

    @media screen and (max-width: 750px) {
        .employee-list, .employee-details {
            width: 100% !important;
        }
    }
    @media screen and (max-width: 600px) {
        .employee-container, .profile{
            flex-direction: column;
        }
        h1 {
            font-size: 20px;
        }
    }
</style>