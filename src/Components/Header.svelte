<script>
    import Experience from './Experience.svelte';
    import Resume from './Resume.svelte';
    import Skills from './Skills.svelte';
    import Footer from './Footer.svelte';

    export let navigate = 1;
</script>

<header>
    <h1>Matthew Vaden</h1>
    <p>Front End Developer</p>
    <nav>
        <ul id="menu">
            <li>
                <a 
                    href="/" 
                    on:click|preventDefault={() => (navigate = 1)}
                    >Skills
                </a>
            </li>
            <li>
                <a 
                href="/" 
                on:click|preventDefault={() => (navigate = 3)}
                >Expereince
            </a>
        </li>
        <li>
            <a 
                href="/" 
                on:click|preventDefault={() => (navigate = 2)}
                >Resume
            </a>
        </li>
        </ul>
    </nav>
</header>

{#if navigate === 1}
<Skills />

{:else if navigate === 2}
<Resume />

{:else if navigate === 3}
<Experience />

{:else}
<h1>Page Not Found</h1>
{/if}


<Footer />

<style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:display=swap');

    h1, li, p, ul {
        font-family: 'Roboto', sans-serif;
        font-weight: 900;
        text-transform: uppercase;
    }

    h1 {
        font-size: 60px;
        letter-spacing: 0.5675rem;
        margin-bottom: 2rem;
    }

    a {
        color: #808080;
        font-weight: 400;
        font-size: 14px;
        letter-spacing: 0.125rem;
    }
    
    a:hover {
        color: #a8a8a8;
        text-decoration: none;
    }

    li {
        list-style: none;
        padding: 0 2rem;
    }

    nav {
        padding: 1.25rem 0;
    }

    p {
        letter-spacing: 8px;
        color: #a8a8a8;
    }

    ul {
        display: flex;
        justify-content: center;
        padding: 0;
    }
</style>