<!-- src/lib/ImageCard.svelte -->

<script>
    export let image; // Image URL prop
    export let title; // Title prop
    export let description; // Description prop
</script>

<div class="card">
    <img src={image} alt={title} />
    <div class="card-content">
        <h2 class="card-title">{title}</h2>
        <p class="card-description">{description}</p>
    </div>
</div>

<style>

.card {
    background-color: #b5e0f2;
    border-radius: 10px;
    overflow: hidden;
    margin: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); 
    flex-direction: row;      /* horizontal layout */
    align-items: center;      /* vertically center content */
}

    .card img {
        width: 120px;    /* fixed width for horizontal layout */
        height: auto;
        flex-shrink: 0;  /* prevent shrinking */
    }

    .card-content {
        flex: 1;         /* take remaining space */
        padding: 15px;
    }

    .card-title {
        font-size: 1.5em;
        color: #333;
        margin: 0 0 10px 0;
    }

    .card-description {
        font-size: 1em;
        color: #666;
        margin: 0;
    }
</style>
