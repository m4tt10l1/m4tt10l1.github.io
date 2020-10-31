---
layout: backend.html
title: backend
slug: backend/backend
# action: https://script.google.com/macros/s/AKfycbx4x-jvzx35vZAUiKHzkeB3hHCbqBPbaR09UD78_o3UtTGaqIM/dev
# action: https://script.google.com/macros/s/AKfycbwoVLxakcPYgo90LbiQ7F2P-ikPeKf3I0F9yFUjFvU/dev
---
<h3>pagine</h3>
<ul>
{% for page in site.pages %}
  <li>{{page.title}} {{page.slug}} </li>
{% endfor %}
  </ul>
  
  <h3>post</h3>
  
<ul>
{% for post in site.posts %}
  <li>{{post.title}} {{post.slug}} </li>
{% endfor %}
  </ul>  
<form action="https://script.google.com/macros/s/AKfycbx4x-jvzx35vZAUiKHzkeB3hHCbqBPbaR09UD78_o3UtTGaqIM/exec" method="post">
<input type="hidden" name="key" value="_data/builder/post-2.json" />
<div>
<label>Risorsa</label> <input type="text" name="resource" value="_data/builder/post-2.json" />
</div>
<div>
  <label>Dati</label> <textarea name="data" cols="50" rows="25">{{ site.data.builder["post-1"] | jsonify }}</textarea>
</div>
<div class="text-center">
  <button name="submit_data" type="submit" class="btn btn-primary">salva</button>
</div>
</form>
