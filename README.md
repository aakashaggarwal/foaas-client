# Foaas Client

[![Build Status](https://travis-ci.org/petedmarsh/foaas-client.png)](https://travis-ci.org/petedmarsh/foaas-client)
[![Code Climate](https://codeclimate.com/github/petedmarsh/foaas-client.png)](https://codeclimate.com/github/petedmarsh/foaas-client)

A client for [FOAAS](http://foaas.com).

## API Version

Version `1.0.0` of the FOAAS API is supported.

## Usage

### Basic Example

```ruby
require 'foaas-client'

fuck = Foaas::Client.new
fuck.off('Bob', 'Alice')
```

### i18n

```ruby
fuck.off('Bob', 'Alice', i18n: :es)
#=> { 'message': 'Vete a la mierda, Bob.', 'subtitle': '-Alice' }
```

### Response Types

```ruby
fuck.off('Bob', 'Alice', type: :html)
#=> '<html>...</html>'

fuck.off('Bob', 'Alice', type: :json)
#=> '{ "message": "Fuck off, Bob.", "subtitle": "- Alice" }'

fuck.off('Bob', 'Alice', type: :jsonp)
#=> 'fuck && fuck({ "message": "Fuck off, Bob.", "subtitle": "- Alice" });'

fuck.off('Bob', 'Alice', type: :text)
#=> 'Fuck off, Bob. - Alice'

fuck.off('Bob', 'Alice', type: :xml)
#=> '<?xml version="1.0" encoding="utf-8"?>...'
```

### Shoutcloud

```ruby
fuck.off('Bob', 'Alice', shoutcloud: true)
#=> { 'message' => 'FUCK OFF, BOB', 'subtitle' => '- ALICE' }
```

### Methods

#### Anyway

```ruby
fuck.anyway('Acme', 'Alice')
#=> { 'message' => 'Who the fuck are you anyway, Acme, why are you stirring up so much trouble, and, who pays you?', 'subtitle' => '- Alice' }
```

#### Awesome

```ruby
fuck.awesome('Alice')
#=> { 'message' => 'This is Fucking Awesome.', subtitle => '- Alice' }
```

#### Back

```ruby
fuck.back('Bob', 'Alice')
#=> { 'message' => 'Bob, back the fuck off.', 'subtitle' => '- Alice' }
```

#### Ballmer

```ruby
fuck.ballmer('Bob', 'Alice', 'Clara')
#=> { 'message' => 'Fucking Bob is a fucking pussy. I'm going to fucking bury that guy, I have done it before, and I will do it again. I'm going to fucking kill Alice.', 'subtitle' => '- Clara' }
```

#### Bday

```ruby
fuck.bady('Bob', 'Alice')
#=> { 'message' => 'Happy Fucking Birthday, Bob', 'subtitle' => '- Alice'}
```

#### Because

```ruby
fuck.because('Alice')
#=> { 'message' => 'Why? Because Fuck you, that\'s why.', 'subtitle' => '- Alice' }
```

#### Bm

```ruby
fuck.bm('Bob', 'Alice')
#=> { 'message' => 'Bravo mike, Bob.', 'subtitle' => '-Alice '}
```

#### Bucket

```ruby
fuck.bucket('Alice')
#=> { 'message' => 'Please choke on a bucket of cocks.', 'subtitle' => '-Alice' }
```

#### Bus

```ruby
fuck.bus('Bob', 'Alice')
#=> { 'message' => 'Christ on a bendy-bus, Bob, don\'t be such a fucking faff-arse', 'subtitle' => '- Alice' }
```

#### Bye

```ruby
fuck.bye('Alice')
#=> { 'message' => 'Fuckity bye!', 'subtitle' => '- Alice' }
```

#### Can I use?

```ruby
fuck.caniuse('Bob', 'Alice')
#=> { 'message' => 'Can you use Bob? Fuck no!', 'subtitle' => '- Alice' }
```

#### Chainsaw

```ruby
fuck.chainsaw('Bob', 'Alice')
#=> { 'message' => 'Fuck me gently with a chainsaw, Bob. Do I look like Mother Teresa?', 'subtitle' => '- Alice' }
```

#### Cool

```ruby
fuck.cool('Alice')
#=> { 'message' => 'Cool story, Bro', '- Alice' }
```

### Dalton

```ruby
fuck.dalton('Bob', 'Alice')
#=> { 'msessage' => 'Bob: A fucking problem solving super-hero', 'subtitle' => '- Alice' }
```

#### Diabetes

```ruby
fuck.diabetes('Alice')
#=> { 'message' => 'I\'d love to stop and chat to you but I\'d rather have type 2 diabetes.', 'subtitle' => '- Alice' }
```

#### Donut

```ruby
fuck.donut('Bob', 'Alice')
#=> { 'message' => 'Bob, go and take a flying fuck at a rolling donut.', 'subtitle' => '- Alice' }
```

#### Do something

```ruby
fuck.dosomething('Write', 'Code', 'Alice')
#=> { 'message' => ' 'Write the fucking code!', 'subtitle' => '- Alice' }
```

#### Everyone

```ruby
fuck.everyone('Alice')
#=> { 'message' => 'Everyone can go and fuck off.', 'subtitle' => '- Alice' }
```

#### Everything

```ruby
fuck.everything('Alice')
#=> { 'message' => 'Fuck everything.', 'subtitle' => '- Alice' }
```

#### Family

```ruby
fuck.family('Alice')
#=> { 'message' => 'Fuck you, your whole family, your pets, and your feces', 'subtitle' => '- Alice'}
```

#### Fascinating

```ruby
fuck.fascinating('Alice')
#=> { 'message' => 'Fascinating story, in what chapter do you shut the fuck up?', 'subtitle' => '- Alice' }
```

#### Field

```ruby
fuck.field('Alice', 'Bob', 'Clara')
#=> { 'message' => 'And Alice said on to Bob, "Verily, cast thine eyes upon the field in which I grow my fucks", and Bobgave witness onto the field, and saw that it was barren.', 'subtitle' => '- Clara' }
```

#### Flying

```ruby
fuck.flying('Alice')
#=> { 'message' => 'I don\'t give a flying fuck.', 'subtitle' => '- Alice' }

#### Gfy

```ruby
fuck.gfy('Bob', 'Alice')
#=> { 'message' => 'Golf foxtrot yankee, Bob.', 'subtilte' => '- Alice' }
```

### Give

```ruby
fuck.give('Alice')
#=> { 'message' => 'I give zero fucks.', 'subtitle' => '- Alice' }
```

#### Greed

```ruby
fuck.greed('greed', 'Alice')
#=> { 'message' => 'The point is, ladies and gentleman, that greed -- for lack of a better word -- is good. :noun is right. greed works. greed clarifies, cuts through, and captures the essence of the evolutionary spirit. greed, in all of its forms -- greed for life, for money, for love, knowledge -- has marked the upward surge of mankind', 'subtitle' => '- Alice'}
```

#### Horse

```ruby
fuck.horse('Alice')
#=> { 'message' => 'Fuck you and the horse you rode in on.', 'subtitle' => '- Alice' }
```

#### Keep

```ruby
fuck.keep('Bob', 'Alice')
#=> { 'message' => 'Bob Fuck off. And when you get there, fuck off from there too. Then fuck off some more. Keep fucking off until you get back here. Then fuck off again', 'subtitle' => '- Alice' }
```

#### Keep calm

```ruby
fuck.keepcalm('paddle', 'Alice')
#=> { 'message' => 'Keep the fuck calm and paddle!', 'subtitle' => '- Alice' }
```

#### King

```ruby
fuck.king('Bob', 'Alice')
#=> { 'message' => 'Oh fuck off, just really fuck off you total dickface. Christ Bob, you are fucking thick.', 'subtitle' => '- Alice' }
```

#### Life

```ruby
fuck.life('Alice')
#=> { 'message' => 'Fuck my life.', 'subtitle' => '- Alice' }
```

#### Linus

```ruby
fuck.linus('Bob', 'Alice')
#=> { 'message' => 'Bob, there aren't enough swear-words in the English language, so now I'll have to call you perkeleen vittupää just to express my disgust and frustration with this crap.', 'subtitle' => '- Alice' }
```

#### Look

```ruby
fuck.look('Bob', 'Alice')
#=> { 'message' => 'Bob, do I look like I give a fuck?', 'subtitle' => '- Alice' }
```

#### Looking

```ruby
fuck.looking('Alice')
#=> { 'message' => 'Looking for a fuck to give.', 'subtitle' => '- Alice' }
```

#### Madison

```ruby
fuck.madison('Bob', 'Alice')
#=> { 'message' => What you\'ve said is one of the most insantely idiotic things I have ever heard, Bob. At no point in your rambling, incoherent response were you even close to anything that could be considered a rational thought. Everyone in this room is now dumber for having listened to it. I award you no points Bob, and may God have mercy on your soul.', 'subtitle' => '- Alice' }
```

### Me

```ruby
fuck.me('Alice')
#=> { 'message' => 'Fuck me.', 'subtitle' => '- Alice'}
```

#### Mornin

```ruby
fuck.mornin('Alice')
#=> { 'message' => 'Happy fuckin\' Morning\'!', 'subtitle' => '- Alice'}
```

#### No

```ruby
fuck.no('Bob', Alice')
#=> { 'message' => 'No fucks given.', 'subtitle' => '- Alice'}
```

#### Nugget

```ruby
fuck.nugget('Bob', 'Alice')
#=> { ''Well Bob, aren\'t you a shining example of a rancid fuck-nugget.', 'subtitle' => '- Alice' }
```

#### Off

```ruby
fuck.off('Bob', 'Alice')
#=> { 'message' => 'Fuck off, Bob.', 'subtitle' => '- Alice' }
```

#### Operations

__Note:__ This is not an "insult" method, it returns the avialble "insult" operations. Additionally, this method only returns JSON.


```ruby
fuck.operations()
#=> [ { 'name' => 'Ballmer', 'url' => '/ballmer/:name/:company/:from', 'fields' => [ { 'name' => 'Name', 'field' => 'name' }, { 'name' => 'Company', 'field' => 'company' }, { 'name' => 'From', 'field' => 'field'} ] }, ...]
```

#### Outside

```ruby
fuck.outside('Bob', 'Alice')
#=> { 'message' => 'Bob, why don\'t you go outside and play hide-and-go-fuck-yourself?', 'subtitle' => '- Alice' }
```

#### Pink

```ruby
fuck.pink('Alice')
#=> { 'message' => 'Well, Fuck me pink.', 'subtitle' => '- Alice' }
```

#### Pulp

```ruby
fuck.pulp('English', 'Alice')
#=> { 'messsage' => 'English, motherfucker, do you speak it?', '- Alice' }
```

#### Retard

```ruby
fuck.retard('Alice')
#=> { 'message' => 'You Fucktard!', 'subtitle' => '- Alice' }
```

#### Sake

```ruby
fuck.sake('Alice')
#=> { 'message' => 'For Fuck's sake!', 'subtitle' => '- Alice'}
```

#### Shakespeare

```ruby
fuck.shakespeare('Bob', 'Alice')
#=> { 'message' => 'Thou clay-brained guts, thou knotty-pated fool, thou whoreson obscene greasy tallow-catch!', 'subtitle' => '- Alice' }
```

#### Shutup

```ruby
fuck.shutup('Bob', 'Alice')
#=> { 'messasge' => 'Bob, shut the fuck up.', 'subtitle' => '- Alice' }
```

#### Single

```ruby
fuck.single('Alice')
#=> { 'message' => 'Not a single fuck was given.', 'subtitle' => '- Alice' }
```

#### Thanks

```ruby
fuck.thanks('Bob', 'Alice')
#=> { 'message' => 'Fuck you very much', 'subtitle' => '- Alice' }
```

#### That

```ruby
fuck.that('Alice')
#=> { 'message' => 'Fuck that', 'subtitle' => '- Alice' }
```

#### Thing

```ruby
fuck.thing('it', 'Alice')
#=> { 'message' => 'Fuck it.', 'subtitle' => '- Alice' }
```

#### Think

```ruby
fuck.think('Bob', 'Alice')
#=> { 'message' => 'Bob, you think I give a fuck?', 'subtitle' => '- Alice' }
```

#### This

```ruby
fuck.this('Alice')
#=> { 'message' => 'Fuck this.', 'subtitle' => '- Alice' }
```

#### Tucker

```ruby
fuck.tucker('Alice')
#=> { 'message' => 'Come the fuck in or fuck the fuck off.', 'subtitle' => '- Alice' }
```

#### Thumbs

```ruby
fuck.thumbs('Alice')
#=> { 'message' => 'Who has two thumbs and doesn't give a fuck? Alice.', 'subtitle' => '- Alice' }
```

#### Version

__Note:__ This is not an "insult" method, it returns the version of the service.

```ruby
fuck.version()
#=> { 'message' => '0.1.0', 'subtitle' => 'FOAAS' }
```

#### What

```ruby
fuck.what('Alice')
#=> { 'message' => 'What the fuck?!', 'subtitle' => '- Alice' }
```

#### Xmas

```ruby
fuck.xmas('Bob', 'Alice')
#=> { 'message' => 'Merry Fucking Christmsa, Bob', 'subtitle' => '- Alice' }
```

#### Yoda

```ruby
fuck.yoda('Bob', 'Alice')
#=> { 'message' => 'Fuck off, you must, Bob', 'subtitle' => '- Alice' }
```

#### You

```ruby
fuck.you('Bob', 'Alice')
#=> { 'message' => 'Fuck you, Bob.', 'subtitle' => '- Alice' }
```

#### Zayn

```ruby
fuck.zayn('Alice')
#=> { 'message' => 'Ask me if I give a motherfuck ?!!', 'subtitle' => '- Alice' }
```

#### Zero

```ruby
fuck.zero('Alice')
#=> { 'message' => 'Zero, thats the number of fucks I give.', 'subtitle' => '- Alice' }
```
