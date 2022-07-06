<script lang="ts">
    const dev = process.env.NODE_ENV === 'development';
    let base = ( dev ? '' : 'Front_SveltKitApp');
</script>


<header>
    <nav class="horizontal-nav">
        <span class="nav-title">Ruslan Khairov</span>
        <div class="right-aligned">
            <a class="btn-link" sveltekit:prefetch href="{base}/">About me</a>
            <a class="btn-link" sveltekit:prefetch href="{base}/funny-fact">Funny fact</a>
        </div>
    </nav>
</header>

<style>
    .horizontal-nav {
        display: flex;
        margin: 0;
        padding: 8px;
        background-color: antiquewhite;
    }

    .nav-title {
        margin: 0;
        font-size: x-large;
        align-self: center;
    }

    .right-aligned {
        display: flex;
        margin-left: auto;
    }

    .btn-link {
        background-color: burlywood;
        padding: 10px 20px;
        margin: 5px;
        text-decoration: none;
    }

    .btn-link:hover {
        background-color: coral;
    }
</style>