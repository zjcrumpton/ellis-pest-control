<script>
    export let activeSubnav;
    export let category;
    const subMenu = {
        education: [{
            name: 'How To Remove Bed Bugs',
            path: '/how-to-remove-bed-bugs'
        },
        {
            name: 'How To Spot Bed Bugs',
            path: '/how-to-spot-bed-bugs'
        },
        {
            name: 'Bed Bug FAQ',
            path: '/faq'
        }  
    ]
    }
</script>
<style>
    .container{
        display: none;
        position: absolute;
        top: 35px;
        padding: 10px 15px;
        background-color: #000;
        z-index: 10;
    }
    ul{
        margin-bottom: 10px;
    }
    li{
        margin-top: 20px;
    }
    a{
        text-decoration: none;
        color: #fff;
    }
    a:hover{
        color: #17ad64;
    }
    .active{
        display: block;
    }
</style>
{#if subMenu[category]}
    <div class='container' class:active={activeSubnav}>
        <ul>
            {#each subMenu[category] as link }
                <li>
                    <a href={"/education" + link.path}>{link.name}</a>
                </li>
            {/each}
        </ul>
    </div>
{/if}