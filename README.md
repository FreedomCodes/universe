# Tris Universe

## Troubleshooting

All the modules have gone through manual unit testing using Swift 3.1 on both macOS and Linux.<br/>
If you use Swift 4 (dev) branch please have a look at [docker images](https://github.com/tris-foundation/docker) to find out<br/>
what snapshot version was used to test all the modules as well as all of the [examples](https://github.com/tris-foundation/examples).

## Current progress
You can track the state of [things here](https://github.com/tris-foundation/universe/projects/1).

Our first goal is to provide a comprehensive foundation for any kind of application,<br/>
from micro service running on IoT device to distributed system designed for high load.<br/>
We can't wait for Swift 5, but when it comes, we will be ready.

## Frontend

> "Standards aren't add-ons to the web. They are the web" - Apple

Over the years we tried to build something more than static web pages, but if we take a step back<br/>
we'll see that all we have is just a workaround for something the web wasn't designed for.<br/><br/>
The web doesn't have a way to build dynamic, composable, rich web applications without use of <br/>
hundreds of kilobytes of javascript hacks.<br/><br/>
No matter how fast our hack around the DOM itself, it still should be downloaded from the server,
get parsed, compiled and executed, and only after that it shines in all of its virtual-beauty. It's still too slow because of its size.<br/><br/>
But hopefully we will soon foret about this like we did with ie6 (sorry for the reminder),<br/>
because all major browser vendors have finally agreed on how the web will look like in the future.<br/>
As some of you may have guessed, we're talking about [Web Components](http://webcomponents.org).
We believe it's the only right way,<br/>
and with [Polymer 2.0](https://www.polymer-project.org/2.0/docs/about_20),
which is almost here, it becomes super easy to do. The future is now.<br/>

## Backend

At the moment we recomend nginx for load balancing,<br>
ssl/tls offloading and for serving static files + [http-server](https://github.com/tris-foundation/http-server) for the API.<br/>
A pure Swift solution will be available after TLS module is ready.<br/>
You can find nginx example [here](https://github.com/tris-foundation/examples/tree/master/spa-nginx).

## Database

If you ok with SQL there is only one open-source enterprise class database available for you today. PostgreSQL.<br/>

But for huge amount of apps we think we can do better. All we need is:<br/>
1. In-memory storage for its hot data.
2. On-disk storage for its cold data.
3. Easy way to work with the data.

And it's obvious these days, we need both of NoSQL and SQL worlds.<br/>
Of course we can use PostgreSQL + Redis or any other combination, but this approach also has downsides:<br/>

1. We have to learn multiple different protocols in addition to SQL.
2. We have to write different logic for those storages.
3. The data is duplicated in both storage systems.
4. The data may become inconsistent.
5. Cold start is very slow.

What we really want:

1. Write Swift code.
2. Done.

Where we are now:

We don't have much resources to implement our own system yet, but fortunately we found [Tarantool](https://tarantool.org).<br/>
In addition to all of its great features, we can also write [stored procedures in Swift](https://github.com/tris-foundation/tarantool#tarantool-module) 🚀 😼

## Contribute

We're very welcome any PRs especially with fixes for grammar and spelling mistakes, <br/>
we make a lot of them because google removed aurebesh translator before we have learned english 🙈 . <br/>
If you think you can improve any sentence, even this one, do it! Many thanks. <br/>

## Further plans

We have a lot on mind. What you see here is just the tip of the iceberg. Stay tuned.

## Be part of something great
You can make a difference. Support us on [BountySource](https://www.bountysource.com/teams/tris). Every contribution counts.
