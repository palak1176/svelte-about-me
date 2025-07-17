<script>
  let name = "Palak Mor"; // Change this to your name
  let favoriteNumber = 16; // Change this to your favorite number
  let bio = "I am from Cumming, Georgia. I am currently a data collection and structuring intern at Syensqo, a multinational material science company. I am super excited to start at Georgia Tech to pursue a major in industrial engineering with a concentration in data analytics and science this fall!";
  let hobbies = ["Diamond Painting", "Listening to Podcasts", "Spending Time with Friends"]; // List some hobbies
    import ImageCard from "./lib/ImageCard.svelte";
  
  let cardData = [
    {
      image:
        "https://mybobbin.com/storage/photo/resized/xy_1300x1000/c/25jieewin008xxe_a9660fb.jpg",
      title: "Diamond Painting",
      description:
        "I love diamond painting! My last painting was a 22 x 28 inch landscape of a balcony overlooking the sea.",
    },
    {
      image: "https://i.scdn.co/image/ab6765630000ba8a4a2f177477ecd05b6f5be8e0",
      title: "Listening to Podcasts",
      description: "I started listening to my favorite podcast, My Favorite Murder by Karen Kilgariff and Georgia Hardstark, 5 years ago.",
    },
    {
      image: "https://i.kickstarter.com/assets/029/996/500/ed20ba38456d6d5caf29e150dbef0522_original.jpg?anim=false&fit=cover&gravity=auto&height=576&origin=ugc&q=92&v=1596039396&width=1024&sig=OD7G8aQ5YMrcc0a31FGgfz3xh2YCnlDw1es9dhwzVDI%3D",
      title: "Spending Time with Friends",
      description:
        "I love hanging out with my friends and taking pictures on our digicams or playing card games like Cabo.",
    },
  ];
  
  </script>

<style>
  .html {
    background-color: rgb(181, 203, 243),
  }
  
  h1 {
    color: #2c3e50;
    font-family: 'Trebuchet MS';
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
    background-color: #3498db;
    color: white;
    padding: 10px 15px;
    border-radius: 5px;
  }
</style>

<div class="html">
<div class="container">
  <h1>About Me</h1>
  <p>Hello, my name is <strong>{name}</strong>!</p>
  <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
  <p>{bio}</p>

  <h2>My Hobbies</h2>
  <div class="hobbies">
    {#each hobbies as hobby}
      <div class="hobby">{hobby}</div>
    {/each}
  </div>
    <h2>Some of My Favorite Things</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
  </div>
</div>