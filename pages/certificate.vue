<template>
    <main class="flex flex-col flex-auto lg:flex-row overflow-hidden bg-gray-900 text-white">
        <div id="mobile-page-title" class="text-center py-4">
            <h2 class="text-2xl font-bold">_certificates</h2>
        </div>

        <div class="flex flex-col w-full overflow-hidden p-5">
            <div id="certificate-case"
                class="grid grid-cols-1 gap-4 lg:grid-cols-4 max-w-full h-full overflow-scroll lg:self-center">
                <div v-for="item in certificateItems" :key="item.title"
                    class="certificate-card p-5 rounded-lg bg-gray-800 shadow-lg transform transition-transform hover:scale-105">
                    <div class="flex items-center mb-3">
                        <img :src="item.icon" alt="icon" class="w-10 h-10 mr-3" />
                        <div>
                            <h4 class="text-md font-semibold">{{ item.title }}</h4>
                            <p class="text-gray-400">{{ item.organization }}</p>
                        </div>
                    </div>
                    <div class="flex justify-between items-center text-sm">
                        <p class="text-gray-400">{{ item.date }}</p>
                        <a :href="item.credentialUrl" target="_blank" class="text-blue-400 underline">Tampilkan
                            kredensial</a>
                    </div>
                    <div v-if="item.skills" class="mt-3 text-sm">
                        <p class="text-gray-400">Keahlian:</p>
                        <ul class="text-gray-400 list-disc list-inside">
                            <li v-for="skill in item.skills" :key="skill">{{ skill }}</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="flex justify-center mt-5 space-x-4">
                <a href="https://www.linkedin.com/in/rafaelnuansa/details/certifications/" target="_blank"
                    class="px-4 py-2 bg-blue-600 rounded-lg hover:bg-blue-700 transition-colors">Lihat sertifikat lainnya di LinkedIn</a>
                <a href="https://santrikoding.com/profile/@rafaelnuansa?tab=certificates" target="_blank"
                    class="px-4 py-2 bg-green-600 rounded-lg hover:bg-green-700 transition-colors">Lihat sertifikat lainnya di SantriKoding</a>
                <a href="https://www.dicoding.com/users/rafaelnuansaramadhon/academies" target="_blank"
                    class="px-4 py-2 bg-gray-600 rounded-lg hover:bg-gray-700 transition-colors">Lihat sertifikat lainnya di Dicoding</a>
            </div>
        </div>
    </main>
</template>

<script setup>
import { ref } from 'vue'

const certificateItems = ref([
    {
        title: "Introduction to Cybersecurity",
        organization: "Cisco",
        date: "Diterbitkan Jan 2024",
        credentialUrl: "https://www.credly.com/badges/679f5f20-1371-4b07-9c69-3ea4ec4c5b07/linked_in_profile",
        icon: "https://media.licdn.com/dms/image/D560BAQHS78gBm1EgiA/company-logo_100_100/0/1719255509518/cisco_logo?e=1729728000&v=beta&t=t4xb4uyIFbeKrdxkCZ6nAOCsMxq2r4Zk2KBGt31bt_o",
    },
    {
        title: "Membangun Website dan Aplikasi Android Desa Dengan Laravel, React.js dan React Native",
        organization: "SantriKoding.com",
        date: "Diterbitkan Sep 2023",
        credentialUrl: "https://santrikoding.com/cek-sertifikat?no=SK-0V9ND81751ARVQQ",
        icon: "https://santrikoding.com/images/favicon.ico",
        skills: ["React Native", "Laravel", "JavaScript", "React.js", "PHP"],
    },
    {
        title: "Membangun Aplikasi dan Website News Dengan Laravel, React.js dan Android",
        organization: "SantriKoding.com",
        date: "Diterbitkan Mei 2023",
        credentialUrl: "https://santrikoding.com/cek-sertifikat?no=SK-LN80M8Q3X12D718",
        icon: "https://santrikoding.com/images/favicon.ico",
        skills: ["React Native", "Laravel", "JavaScript", "React.js", "PHP"],
    },
    {
        title: "Membangun Smart Home System Dengan Laravel, React Native dan NodeMCU",
        organization: "SantriKoding.com",
        date: "Diterbitkan 2024",
        credentialUrl: "https://santrikoding.com/cek-sertifikat?no=SK-0V1YB20T8X7TVN6",
        icon: "https://santrikoding.com/images/favicon.ico",
        skills: ["React Native", "Laravel", "JavaScript", "React.js", "PHP"],
    },
    {
        title: "Sertifikat Kelas Belajar Docker untuk Pemula",
        organization: "CODEPOLITAN",
        date: "Diterbitkan Okt 2022 Kedaluwarsa Okt 2025",
        credentialUrl: "https://codepolitan.com/c/W3BLMCL",
        icon: "https://www.codepolitan.com/favicon.ico",
        skills: ["Pengembangan Web"],
    },
    {
        title: "Sertifikat Kelas Belajar Go-Lang untuk Pemula",
        organization: "CODEPOLITAN",
        date: "Diterbitkan Okt 2022 Kedaluwarsa Okt 2025",
        credentialUrl: "https://codepolitan.com/c/PDY12NT",
        icon: "https://www.codepolitan.com/favicon.ico",
        skills: ["Pengembangan Web"],
    },
    {
        title: "Sertifikat Kelas Belajar JavaScript Async",
        organization: "CODEPOLITAN",
        date: "Diterbitkan Okt 2022 Kedaluwarsa Okt 2025",
        credentialUrl: "https://codepolitan.com/c/1H4PS8J",
        icon: "https://www.codepolitan.com/favicon.ico",
        skills: ["Pengembangan Web"],
    },
    {
        title: "Sertifikat Kelas Belajar Go-Lang untuk Pemula",
        organization: "CODEPOLITAN",
        date: "Diterbitkan Okt 2022 Kedaluwarsa Okt 2025",
        credentialUrl: "https://codepolitan.com/c/PDY12NT",
        icon: "https://www.codepolitan.com/favicon.ico",
        skills: ["Pengembangan Web"],
    },
    // Tambahkan sertifikat lainnya sesuai kebutuhan...
])
</script>

<style>
#certificate-case {
    padding: 25px 25px 5px;
}

.certificate-card {
    background-color: #1C2B3A;
}

@media (max-width: 768px) {
    #certificate-case {
        padding: 0px 25px 40px;
    }
}

@media (min-width: 768px) {
    #certificate-case {
        padding: 50px 50px 40px;
    }
}

@media (min-width: 1350px) {
    #certificate-case {
        padding: 50px 80px 40px;
    }
}
</style>