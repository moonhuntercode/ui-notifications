<script>
import campana from '../assets/campana-icon-notifications-no-active.svg'
import campanaActive from '../assets/campana-icon-notifications-active.svg'
  import { onMount } from 'svelte';
  let count2=0;
$:notifications = count2;
let existe= false;
function increment() {
    count2+=1;
    console.log(count2);
}
createNumber(Element){

}
  onMount(() => {
    document.querySelectorAll('img').forEach(element => {
        element.addEventListener('click', (event) => {
            
            // recognize the target, the actual image
            console.log(event.target);
            console.log(document.querySelector('#redondo').style.visibility="visible");
          
        })
    })
})
</script>

<nav id="navbar">
    
        <button on:click={increment}>
  <img src={notifications == 0 ? campana : campanaActive} id="campana-icon" alt="campana">
  <div id="redondo">
      
    </div>
</button>
    
    <h1>Navbar</h1>
</nav>