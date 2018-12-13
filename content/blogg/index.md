---
views:
    main:
        template: anax/v2/article/default
        data:
            class: blog

    byline: false
    block-about: false
    article-toc: false

    blog-list:
        region: main
        template: anax/v2/blog-list/default
        sort: 2
        data:
            dateFormat: j F Y
            meta: 
                type: toc
                orderby: publishTime
                orderorder: desc

    blog-toc:
        region: sidebar-right
        template: anax/v2/blog-toc/default
        sort: 2
        data:
            title: Innehåll
            meta: 
                type: copy
                view: blog-list

---
Dagens Bild
===========================

I denna bloggen så lägger jag upp bilder jag tagit på semestrar, utflykter, etc. Bilderna kommer även redigeras lite för att se olika effekter och hur de kan påverka bilderna.
