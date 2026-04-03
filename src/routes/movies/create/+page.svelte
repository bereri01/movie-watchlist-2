<script>
  export let data;
</script>

<div class="container my-4">
  <a href="/movies" class="btn btn-outline-light btn-sm mb-4">Back to Movies</a>

  <div class="card bg-dark text-white shadow-lg">
    <form method="POST" action="?/create">
      <div class="col-md-8">
        <div class="card-body p-4">
          <h1 class="card-title display-5 fw-bold mb-3">Add a Movie</h1>
          <hr class="border-secondary" />
          <ul class="list-unstyled mt-3 fs-5">
            <li class="mb-2">
              <span class="text-secondary">Title:</span>
              <input name="title" class="form-control" type="text" />
            </li>
            <li class="mb-2">
              <span class="text-secondary">Year:</span>
              <input name="year" class="form-control" type="number" />
            </li>
            <li class="mb-2">
              <span class="text-secondary">Length:</span>
              <input name="length" class="form-control" type="text" />
            </li>
          </ul>
          <button type="submit" class="btn btn-outline-light btn-sm mb-4">Add Movie</button>
        </div>
      </div>
    </form>
  </div>
</div>
