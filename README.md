# Content-Management-Tool-
Here's an example of a basic web page using HTML, CSS, and JavaScript that allows to add text, images, videos, and other elements to create a blog-like content management tool. Please note that this is a simplified example .
<!DOCTYPE html>
<html>
<head>
  <title>Blog Content Management Tool</title>
  <style>
    .content-container {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .element-container {
      width: 80%;
      margin-bottom: 20px;
    }

    .element-container label {
      display: block;
      margin-bottom: 5px;
    }

    .element-container input,
    .element-container textarea {
      width: 100%;
      padding: 5px;
      font-size: 16px;
    }

    .element-container button {
      padding: 5px 10px;
      font-size: 16px;
    }

    #blog-preview {
      border: 1px solid #ccc;
      padding: 10px;
      margin-top: 20px;
      width: 80%;
    }
  </style>
</head>
<body>
  <div class="content-container">
    <div class="element-container">
      <label for="blog-title">Title:</label>
      <input type="text" id="blog-title" placeholder="Enter the title">
    </div>
    <div class="element-container">
      <label for="blog-image">Image URL:</label>
      <input type="text" id="blog-image" placeholder="Enter the image URL">
    </div>
    <div class="element-container">
      <label for="blog-content">Content:</label>
      <textarea id="blog-content" rows="6" placeholder="Enter the content"></textarea>
    </div>
    <div class="element-container">
      <label for="blog-video">Video URL:</label>
      <input type="text" id="blog-video" placeholder="Enter the video URL">
    </div>
    <div class="element-container">
      <button onclick="addBlog()">Add Blog</button>
    </div>
    <div id="blog-preview"></div>
  </div>

  <script>
    function addBlog() {
      const title = document.getElementById('blog-title').value;
      const image = document.getElementById('blog-image').value;
      const content = document.getElementById('blog-content').value;
      const video = document.getElementById('blog-video').value;

      const blogPreview = document.getElementById('blog-preview');
      blogPreview.innerHTML += `
        <h2>${title}</h2>
        <img src="${image}" alt="${title}" style="max-width: 100%;">
        <p>${content}</p>
        <iframe width="560" height="315" src="${video}" frameborder="0" allowfullscreen></iframe>
        <hr>
      `;
    }
  </script>
</body>
</html>
