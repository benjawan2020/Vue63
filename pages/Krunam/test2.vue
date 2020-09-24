<template>
    <div>
        <h1>ข้อมูลนักศึกษา</h1>
        <ul>
            <li v-for="st in student" :key="st.code">
                <span>{{st.code}}</span>
                <span>{{st.name}}</span>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    data(){
        return{
            student:[
                {code: '6239010001', name: 'โยธิน'},
                {code: '6239010002', name: 'มินตรา'},
                {code: '6239010003', name: 'พรกมล'},
            ]
        }
    }
}
</script>