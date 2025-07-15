<script>
  let name = "Sherlyn"; // Change this to your name
  let favoriteNumber = 10; // Change this to your favorite number
  let bio = "I am a software engineer exploring new tech tools !";
  let hobbies = [
    "Coding 👩🏻‍💻",
    "Cooking 🥘",
    "Drinking Coffee ☕️",
    "Making music 🎧 ",
  ]; // List some hobbies

  import ImageCard from "./lib/ImageCard.svelte";

  let cardData = [
    {
      image:
        "https://media.istockphoto.com/id/185590965/photo/yellow-rubber-duck-for-bath-time.jpg?s=612x612&w=0&k=20&c=QoT-O5jbOugCgdQhLat15c0L9jCmRrSTiO9U50W_eQc=",
      title: "Coding",
      description:
        "I love solving problems and writing code to build cool things.",
    },
    {
      image:
        "https://media.istockphoto.com/id/1460007178/photo/library-books-on-table-and-background-for-studying-learning-and-research-in-education-school.jpg?s=612x612&w=is&k=20&c=PvjSrEGbw3G64q74ccIQaJ9nEj9AzPwjvRo1cWFA3UU=",
      title: "Reading",
      description: "Books help me grow intellectually and creatively.",
    },
    {
      image:
        "https://media.istockphoto.com/id/1440399157/photo/international-airport-terminal-asian-beautiful-woman-with-luggage-and-walking-in-airport.jpg?s=612x612&w=0&k=20&c=RqmI0KG_pnEb_GmWLC6pY5MoV75JBt1nU1L9dStkJys=",
      title: "Traveling",
      description:
        "I enjoy exploring new cultures and learning from the world around me.",
    },
  ];
</script>

<main>
  <h1>Vite + Svelte</h1>
  <div class="container">
    <h2>About Me</h2>
    <p>Hello, my name is <strong>{name}</strong>!</p>
    <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
    <p>{bio}</p>

    <h2>My Hobbies</h2>
    <div class="hobbies">
      {#each hobbies as hobby}
        <div class="hobby">{hobby}</div>
      {/each}
    </div>
  </div>

  <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</main>

<style>
  h1 {
    color: #f50762;
    font-family: Arial, sans-serif;
  }
  h2 {
    color: rgb(3, 0, 4);
  }
  p {
    color: black;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .hobbies {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .hobby {
    background-color: #0101ff;
    color: rgb(243, 242, 245);
    padding: 10px 15px;
    border-radius: 5px;
  }
  main {
    padding-top: 200px;
    padding-bottom: 200px;
    padding-left: 200px;
    padding-right: 200px;
    background-color: rgb(124, 168, 255);
  }
</style>
