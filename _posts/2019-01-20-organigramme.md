---
title: Exemple d'un organigramme
layout:
---

<!-- https://github.com/fperucic/treant-js/tree/master/examples/basic-example -->

<meta name="viewport" content="width=device-width">
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">

<link rel="stylesheet" href="/assets/css/vendor/treant/Treant.css" type="text/css"/>
<link rel="stylesheet" href="/assets/css/vendor/treant/basic-example.css" type="text/css"/>

<script src="/assets/js/vendor/treant/vendor/raphael.js"></script>
<script src="/assets/js/vendor/treant/Treant.js"></script>

<div id="basic-example"> </div>


<script>

var tmp_img_url = function(idx) {
	return "http://fperucic.github.io/treant-js/examples/headshots/" + idx + ".jpg"
}

var chart_config = {
    chart: {
        container: "#basic-example",

        connectors: {
            type: 'step'
        },
        node: {
            HTMLclass: 'nodeExample1'
        }
    },
    nodeStructure: {
        text: {
            name: "Maud et Annika",
            title: "Co-présidence",
            contact: "Tel: 01 213 123 134",
        },
        image: tmp_img_url(4),
        children: [
            {
                text:{
                    name: "???",
                    title: "Secrétaire",
                },
                image: tmp_img_url(1),
            },
            {
                text:{
                    name: "???",
                    title: "Trésorière",
                },
                image: tmp_img_url(5),
            },
            {
                text:{
                    name: "Flavia",
                    title: "Responsable poulailler",
                    contact: "Tel: 01 213 123 134",
                },
								stackChildren: true,
                image: tmp_img_url(10),
                children: [{
                    text:{
                        name: "Benjamin",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(6),
                }, {
                    text:{
                        name: "Sandrine",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(10),
                }, {
                    text:{
                        name: "Benjamin",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(6),
                }, {
                    text:{
                        name: "Sandrine",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(10),
                }, {
                    text:{
                        name: "Benjamin",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(6),
                }, {
                    text:{
                        name: "Sandrine",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(10),
                }, {
                    text:{
                        name: "Benjamin",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(6),
                }, {
                    text:{
                        name: "Sandrine",
                        title: "Membre poulailler"
                    },
                    link: {
                        href: "/"
                    },
                    image: tmp_img_url(10),
                }



                ]
            },
            {
                text:{
                    name: "Thomas ?",
                    title: "Responsable jardins",
                    contact: "Tel: 01 213 123 134",
                },
                stackChildren: true,
                image: tmp_img_url(2),
                children: [
                    {
                        text:{
                            name: "Benjamin",
                            title: "Membre jardin"
                        },
                        link: {
                            href: "/"
                        },
                        image: tmp_img_url(6),
                    },
                    {
                        text:{
                            name: "Jean-Charles et Françoise",
                            title: "Membre jardin"
                        },
                        link: {
                            href: "/"
                        },
                        image: tmp_img_url(7),
                    }
                ]
            }
        ]
    }
};

var my_chart = new Treant(chart_config);
</script>
