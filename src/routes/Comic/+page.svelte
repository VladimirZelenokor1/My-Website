<script lang='ts'>
    import { onMount } from 'svelte';
    
    interface XKCD {
      title: string;
      img: string;
      alt: string;
      year: string
      month: string;
      day: string;
    }
    
    async function fetchSomeNumber() {
    const params = new URLSearchParams();
    return fetch('https://fwd.innopolis.app/api/hw2?email=v.zelenokor@innopolis.university' + params.toString()).then(r => r.json());
    }

    async function fetchImage(id:number) {
        const params = new URLSearchParams();
        return fetch('https://getxkcd.vercel.app/api/comic?num=' + id + params.toString()).then(r => r.json());
    }
    
    export let comic: XKCD = {
      title: '', img: '', alt: '',
      year: '', month: '', day: ''
    };

    export let getDate: string = '';

    onMount(async () => {
    const id = await fetchSomeNumber();
    const image = await fetchImage(id);
    comic = image;
    getDate = new Date(parseInt(comic.year), parseInt(comic.month), parseInt(comic.day)).toLocaleDateString(undefined, { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' })
    });
  </script>
  <div>
    <h1>Title: {comic.title}</h1>
    <p>Alt: {comic.alt}</p>
    <p>Date: {getDate}</p>
    <img style="display: block; margin-left:auto; margin-right:auto; width:fit-content" src={comic.img} alt={comic.alt}/>
  </div>

