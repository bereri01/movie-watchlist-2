<script>
  export let data;
</script>


<div class="container my-4">
  <a href="/movies" class="btn btn-outline-light btn-sm mb-4">Back to Movies</a>

  <div class="card bg-dark text-white shadow-lg">
    <div class="row g-0">

      <div class="col-md-4">
        <img
          src={data.movie.poster}
          alt={data.movie.title}
          class="img-fluid rounded-start h-100"
          style="object-fit: cover;"
        />
      </div>

      <div class="col-md-8">
        <div class="card-body p-4">
          <h1 class="card-title display-5 fw-bold mb-3">{data.movie.title}</h1>
          <hr class="border-secondary" />
          <ul class="list-unstyled mt-3 fs-5">
            <li class="mb-2">
              <span class="text-secondary">Jahr</span>
              <strong>{data.movie.year}</strong>
            </li>
            <li class="mb-2">
              <span class="text-secondary">Dauer</span>
              <strong>{data.movie.length}</strong>
            </li>
            <li class="mb-2">
              <span class="text-secondary">Cast</span>
              <strong>{data.movie.actors.join(", ")}</strong>
            </li>
          </ul>
          <form method="POST" action="?/delete">
            <input type="hidden" name="id" value={data.movie._id} />
            <button class="btn btn-danger btn-sm mb-4">Delete Movie</button>
          </form>
        </div>
      </div>
    
    </div>
    
  </div>
</div>