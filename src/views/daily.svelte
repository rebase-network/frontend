<script>
  import { onMount } from "svelte";
  // const url = "http://db.rebase.network/web3daily/public/posts?_order=-id,-time&_page_size=10&_page=1"

  // let posts = [];

  // const opts =  {
  //   'Content-Type': 'application/json'
  // }
</script>

<main class="container">
  <div class="row mb-2">
    <div class="col-md-10">
      <form action="" method="post">

        <div class="row mb-3">
          <label for="" class="col-sm-2 col-form-label">发送者</label>
          <div class="col-sm-10">
            <select class="form-select" name="editor">
              <option value="nana">娜娜</option>
              <option value="rebecca">Rebecca</option>
              <option value="nicole">Nicole</option>
              <option value="jasmyn">Jasmyn</option>
              <option value="ryan">黄岩Ryan</option>
              <option value="gala">gala</option>
              <option value="river">river</option>
              <option value="frozen">frozen</option>
              <option value="harry">harry</option>
              <option value="liuyi">刘一</option>
              <option value="shooter">shooter</option>
            </select>
          </div>
        </div>


        <div class="row mb-3">
          <label for="" class="col-sm-2 col-form-label">作者</label>
          <div class="col-sm-10">
            <input type="text" class="form-control" name="author1" placeholder="作者" required>
          </div>
        </div>

        <div class="row mb-3">
          <label for="" class="col-sm-2 col-form-label">标题</label>
          <div class="col-sm-10">
            <input type="text" class="form-control" name="title1" placeholder="标题" required>
          </div>
        </div>

        <div class="row mb-3">
          <label for="" class="col-sm-2 col-form-label">链接</label>
          <div class="col-sm-10">
            <input type="text" class="form-control" name="url1" placeholder="链接" required>
          </div>
        </div>

        <div class="row mb-3">
          <label class="col-sm-2 col-form-label" for="">介绍</label>
          <div class="col-sm-10">
            <textarea class="form-control" name="introduce1" rows="2"></textarea>
          </div>
        </div>

        <div class="row">
          <div class="col-sm-10 offset-sm-2">
            <button type="submit" class="btn btn-primary">发布</button>
          </div>
        </div>
      </form>


    </div>

    <!-- <div class="col-md-6">
      <iframe src="https://rebase.network/posts/category/web3daily" frameborder="0" width="90%" height="600" title="Rebase">
      </iframe>
    </div> -->
  </div>

</main>
