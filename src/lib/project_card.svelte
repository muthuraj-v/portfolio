<script lang="ts">
  export let title: string;
  export let description: string;
  export let stack: string;
  export let link: string;
</script>

<a class="card" href={link} target="_blank" rel="noopener noreferrer">
  <h3>{title}</h3>
  <p>{description}</p>
  <span>{stack}</span>
</a>

<style>
  .card {
    display: block;
    padding: 25px;
    border-radius: 12px;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    transition: 0.3s;
    text-decoration: none;
    color: inherit;
  }

  .card:hover {
    transform: translateY(-6px);
    background: rgba(255, 255, 255, 0.08);
  }

  .card h3 {
    margin-bottom: 10px;
  }

  .card p {
    opacity: 0.7;
    margin-bottom: 10px;
  }

  .card span {
    font-size: 14px;
    opacity: 0.6;
  }
</style>
