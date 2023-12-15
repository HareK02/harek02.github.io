<script lang="ts">
</script>

<div class="root">
    <div class="card">
        <img src="images/HareIcon.png" alt="logo" height="128" />
        <div class="copyright">
            <p>© Hare 2023</p>
        </div>
    </div>
    <div class="separator"></div>
    <div class="links">
        <ul>
            <li>
                <h4>Links</h4>
            </li>
            <li>
                <a> About </a>
            </li>
            <li>
                <a> Contact </a>
            </li>
            <li>
                <a> Projects </a>
            </li>
            <li>
                <a> Blog </a>
            </li>
        </ul>
        <ul>
            <li>
                <h4>Socials</h4>
            </li>
            <li>
                <a> Instagram </a>
            </li>
            <li>
                <a> YouTube </a>
            </li>
        </ul>
    </div>
</div>

<style lang="scss">
    .root {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        color: white;
        padding: 1rem;
        height: 16rem;
    }
    .card {
        height: 100%;
        margin: 1rem;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }
    .copyright {
        margin: 1rem;
    }
    .separator {
        height: 100%;
        width: 1px;
        background-color: #fffa;
        margin: 1rem;
    }
    .links {
        height: 100%;
        display: flex;
        flex-direction: row;
        justify-content: start;
        align-items: top;
    }
    ul {
        list-style: none;
    }
    a {
        color: white;
				padding: 0.5rem;
    }
</style>
