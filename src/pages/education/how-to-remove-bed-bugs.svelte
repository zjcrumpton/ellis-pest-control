<script>
    import EducationLayout from './index.svelte'
    let content = 'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.'
</script>
<style>
    section{
        width: 70%;
        margin: 0 auto;
        padding-top: 80px;
        color: #fff;
    }
    header{
        padding: 10px;
        border-bottom: 1px dotted #ccc;
    }
    h2{
        font-size: 1.5em;
    }
    article{
        padding: 10px;
    }
    article div{
        line-height: 1.5em;
    }
</style>
<EducationLayout>
    <section>
        <header>
            <h2>How to remove </h2>
        </header>
        <article>
            <div>{content}</div>
        </article>
    </section>
</EducationLayout>