# gothub

A convenience wrapper for [`got`](https://github.com/sindresorhus/got) to interact with the [GitHub API](https://developer.github.com/v3/), very similar to [gh-got](https://github.com/sindresorhus/gh-got).


## Install

```
$ npm install --save gothub
```

## Usage

With [gh-got](https://github.com/sindresorhus/gh-got), you do this:

```js
var ghGot = require('gh-got');

ghGot('users/sindresorhus', {token: 'foo'}, function(err, data){
  console.log(data.login); //=> 'sindresorhus'
});
```

With [gothub](https://github.com/flesch/gothub), you can do this:

```js
var gothub = require('gothub');

var github = new gothub({ token:'foo', endpoint:'https://github-enterprise.example.com/api/v3' });

github.get('users/sindresorhus', function(err, data){
  console.log(data.login); //=> 'sindresorhus'
});
```

[gothub](https://github.com/flesch/gothub) moves the `token` and `endpoint` options into the constructor.

---

Much of the work was shamelessly borrowed from [Sindre Sorhus](http://sindresorhus.com) - I simply rearranged some things.
