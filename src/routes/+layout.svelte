<script lang="ts">
    import "./layout.css";
    import favicon from "$lib/assets/favicon.svg";

    let { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={favicon} />
    <title>Smith Laundry - บริการซักรีดเสื้อผ้า</title>
    <meta
        name="description"
        content="Smith Laundry ร้านซักรีดเสื้อผ้าที่ให้บริการด้วยความใส่ใจ ผ้าสะอาด หอม นุ่ม พร้อมส่งมอบความสดใสให้กับทุกชิ้นผ้าของคุณ"
    />
    <meta
        name="keywords"
        content="ซักรีดเสื้อผ้า, บริการซักรีดเสื้อผ้า, ซักรีดเสื้อผ้า, ร้านซักรีด"
    />
    <meta name="author" content="Smith Laundry" />

    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website" /> 
    <meta property="og:title" content="Smith Laundry - บริการซักรีดเสื้อผ้า" />
    <meta
        property="og:description"
        content="Smith Laundry ร้านซักรีดเสื้อผ้าที่ให้บริการด้วยความใส่ใจ ผ้าสะอาด หอม นุ่ม พร้อมส่งมอบความสดใสให้กับทุกชิ้นผ้าของคุณ"
    />
    <meta property="og:image" content="/images/result1.png" />

    <!-- Canonical URL -->
    <link rel="canonical" href="https://laundry-shop.pages.dev/" />
</svelte:head>

{@render children()}
