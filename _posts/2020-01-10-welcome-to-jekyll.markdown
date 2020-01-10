---
layout: post
title:  "How to write a glTF2 model loader"
date:   2020-01-10 14:52:02 -0700
categories: gltf2 github programming
---
Jekyll also offers powerful support for code snippets:

{% highlight java %}
  public GLTF load(URI uri) throws IOException {
    GLTF gltf = new GLTF(streamIO, uri);

    ObjectReader reader = mapper.setInjectableValues(injectGLTF(gltf)).readerForUpdating(gltf);
    reader.readValue(streamIO.getStreamForResource(uri));

    return gltf;
  }
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
