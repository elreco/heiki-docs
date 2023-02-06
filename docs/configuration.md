# 🔧 Configuration

### Main configuration

You can find the file \`config.json\` at the of the project. This is the main configuration file, it will allow you to easily configure your entire site

```json
{
  "isProduction": true,
  "appName": "Heiki",
  "appDescription": "3333 female warriors picked up their weapons to fight for this world.",
  "appUrl": "https://demo.heikinft.com",
  "twitter": "https://twitter.com/HeikiNFT",
  "discord": "https://discord.gg/heikinft",
  "opensea": "https://opensea.io/collection/official-heiki-nft",
  "s3": "https://heiki.ams3.digitaloceanspaces.com",
  "infuraUrl": "https://mainnet.infura.io/v3/d056f2baa7be43ecad64ad8b05b89a4e",
  "presaleMintDate": "June 24, 2023 18:00:00",
  "mintDate": "June 25, 2023 18:00:00",
  "mintStatus": 1,
  "maxSupply": 3333,
  "maxMint": 2,
  "presaleMaxMint": 1,
  "presaleMintPrice": 0.065,
  "mintPrice": 0.08,
  "googleAnalyticsId": ""
}
```

**mintStatus**:

* `0` is the default status, mint is not available and there is a countdown set by `presaleMintDate`
* `1` is the presale mint
* `2` is the public sale

**s3:**

Here is the s3 link. You must upload important files:

* a file called `wl.json` including an array of whitelisted address, ex:

```json
[
  "0x95aBA4e8FEb22D93EC9A5379D2fabefC888AEdEB"
]
```

*   a file called `_metadata.json` including the metadatas of your collections, ex:\
    \


    ```json
    [
      {
        "name": "Heiki #150",
        "description": "244 female warriors picked up their weapons to fight for this world, against oppression and bring peace to this world once again.",
        "image": "ipfs://QmTeRR7ditsKdZeiFEDB8NQN3ZhmnAcsywUcCAKu3QbRQJ/150.png",
        "attributes": [
          {
            "trait_type": "Background",
            "value": "Yellow"
          },
          {
            "trait_type": "Pattern",
            "value": "Sakura"
          },
          {
            "trait_type": "Body",
            "value": "Choco"
          },
          {
            "trait_type": "Clothes",
            "value": "Flower Kimono"
          },
          {
            "trait_type": "Expressions",
            "value": "Sad"
          },
          {
            "trait_type": "Eyes",
            "value": "Green"
          },
          {
            "trait_type": "Eye Accessory",
            "value": "Glasses"
          },
          {
            "trait_type": "Hair",
            "value": "Blue Tied"
          },
          {
            "trait_type": "Earring",
            "value": "Katana"
          },
          {
            "trait_type": "Weapon",
            "value": "Wood Katana"
          }
        ]
      },
      {
        "name": "Heiki #36",
        "description": "244 female warriors picked up their weapons to fight for this world, against oppression and bring peace to this world once again.",
        "image": "ipfs://QmTeRR7ditsKdZeiFEDB8NQN3ZhmnAcsywUcCAKu3QbRQJ/36.png",
        "attributes": [
          {
            "trait_type": "Background",
            "value": "Grey"
          },
          {
            "trait_type": "Pattern",
            "value": "Awanochi"
          },
          {
            "trait_type": "Body",
            "value": "Choco"
          },
          {
            "trait_type": "Clothes",
            "value": "Blue Kimono"
          },
          {
            "trait_type": "Expressions",
            "value": "Angry"
          },
          {
            "trait_type": "Eyes",
            "value": "Green"
          },
          {
            "trait_type": "Hair",
            "value": "Red Bun"
          },
          {
            "trait_type": "Earring",
            "value": "Samurai Ring"
          },
          {
            "trait_type": "Mask",
            "value": "Full"
          },
          {
            "trait_type": "Weapon",
            "value": "Golden Kunai 2"
          }
        ]
      }
    ```



* Then you can upload your NFT images, ex:\
  \
  [https://heiki.ams3.digitaloceanspaces.com/1.png](https://heiki.ams3.digitaloceanspaces.com/1.png)\
  [https://heiki.ams3.digitaloceanspaces.com/2.png](https://heiki.ams3.digitaloceanspaces.com/1.png)\
  ...\
  [https://heiki.ams3.digitaloceanspaces.com/101.png](https://heiki.ams3.digitaloceanspaces.com/1.png)\


#### Customize Images

You can find all the images in the `/public` folder.

#### Team, FAQ and Roadmap configurations

#### FAQ

Go to `/components/faq.js`\
\
You will find a constant variable called \`faqs\` that looks like this:

```javascript
const faqs = [
  {
    id: 2,
    question: 'Is there a Mint price?',
    answer: config.mintPrice
  },
  {
    id: 3,
    question: 'What blockchain is the project on?',
    answer: 'ETH - MetaMask'
  },
  {
    id: 4,
    question: 'How to get WL on the server?',
    answer:
      'Be active in the discord chat and spread love so we can see you !'
  },
  {
    id: 5,
    question: 'How many warriors there will be?',
    answer: '3333 NFTs including 10 1/1 art pieces.'
  },
  {
    id: 6,
    question: 'Can I lose the OG / WL role?',
    answer:
      'We are focusing on growing an organic community. Be yourself, be active, spread love and it should be alright.'
  },
  {
    id: 7,
    question: 'How will the mint go?',
    answer: 'Pre sale for OGs and WLs + Public sale for leftover.'
  }
]
```

#### Roadmap

Go to `/components/roadmap.js`\
``\
``You will find a constant variable called \`roadmap\` that looks like this:

```javascript
const roadmapSteps = [
  {
    id: 1,
    title: 'Our mission',
    src: Icon1,
    link: 'https://www.missionimpossible.com',
    description: (
      <>
        <p>
          <strong className="text-tomoe">Absolute power</strong> With broken
          timelines happening in the 11th century, the great battle is about
          to begin. A mass of people, fuelled by greed, annihilated humanity,
          and obtained power, great enough to establish the new order.
        </p>
        <p>
          Our mission is to release{' '}
          <strong className="text-tomoe">3333</strong> female warriors with
          around 300 unique traits.{' '}
          <strong className="text-tomoe">Heiki</strong> is not just PFP NFT,
          it is also a brand and to become a major brand to exist in the
          digital/NFT space and lifestyle industries.
        </p>
      </>
    )
  },
  {
    id: 2,
    title: 'Community',
    src: Icon2,
    link: 'https://www.missionimpossible.com',
    description: (
      <p>
        Our focus is to <strong className="text-tomoe">connect people</strong>{' '}
        together in web3 and we believe that community play an important role
        in the success of the NFT project. When you join our community, your
        voice matters, and you will be able to vote based on the number of
        tokens you hold. The intent has always been to connect the community
        and build the community focuses which connect us with inspiring
        individuals. You have the word of the team that we will continue to
        build and create for the community, but we do not promise any future
        value of the NFT.
      </p>
    )
  },
  {
    id: 3,
    title: 'Branding',
    src: Icon3,
    link: 'https://www.missionimpossible.com',
    description: (
      <p>
        Heiki will have their own brand apparel and the first{' '}
        <strong className="text-tomoe">333 minters</strong> will get a
        high-quality tee collection for free (Shipping included)
      </p>
    )
  },
  {
    id: 4,
    title: 'Transparency',
    src: Icon4,
    link: 'https://www.missionimpossible.com',
    description: (
      <p>
        We will allocate <strong className="text-tomoe">25%</strong> of the
        minted to Community wallet which will be known as the “Heiki
        Treasure”. Additionally,{' '}
        <strong className="text-tomoe">30% of all Gen 1</strong> secondary
        markets will go towards Heiki Treasure. Heiki Treasure will be used to
        fund projects detailed on the roadmap.
      </p>
    )
  },
  {
    id: 5,
    title: 'Staking system',
    src: Icon5,
    link: 'https://www.missionimpossible.com',
    description: (
      <p>
        Throughout Japan’s history, Samurai were paid by their feudal lords,
        the Daimyo, in rice or land. We want to reward our holders by
        implementing staking system. We will launch a utility token and
        holders will be able to stake their Heiki avatars to claim{' '}
        <strong className="text-tomoe">$Rice</strong> token which can be used
        to claim <strong className="text-tomoe">3D version NFT</strong>,
        Hoodies, Tees, including{' '}
        <strong className="text-tomoe">Gen 2 release</strong> can be paid
        partially with our tokens, more utilities will come in roadmap 2.0.
      </p>
    )
  },
  {
    id: 6,
    title: 'Manga',
    src: Icon6,
    link: 'https://www.missionimpossible.com',
    description: (
      <p>
        Our team has been working on developing{' '}
        <strong className="text-tomoe">the Heiki concept</strong> and story.
        We will release our manga series and all female warrior characters in
        the manga will be in the Heiki collection. For the first chapter, we
        will pick characters based on voting systems or through a community
        raffle and the raffle winner will have their characters used for our
        first chapter manga series.
      </p>
    )
  }
]
```

#### Team

Go to \`/components/team.js\`\
\
You will find a constant variable called \`members\` that looks like this:

```javascript
const members = [
    {
      id: 1,
      pseudo: 'Kyosuke Rogue',
      name: 'Arghi Pratama',
      src: Profile1,
      twitter: 'bangwest06',
      instagram: 'pratamaarghi',
      title: 'Co-founder',
      description: (
        <>
          <p>
            My name is Arghi Pratama and I&apos;m 26 years old. I am originally
            from Indonesia but I have been living in Queenstown, New Zealand
            since 2015.
          </p>
          <p>
            I met @Sune&apos;emon Torii in 2015 when we were studying together
            and we have been become a really good friend. He is my mentor and he
            taught me about crypto !! I have been investing in crypto since 2018
            and NFT since July in 2021 last year. 📊
          </p>
          <p>
            I met @Shiro Kujira in 2020 and we become close friend too, we both
            love nature so much which is the reason I love hiking. Mostly during
            our day off, we spend the day hiking to see nature and beautiful
            scenery in South Island, New Zealand. 🏔️
          </p>
          <p>
            Besides that, I am continuing my study computer science field since
            2021.
          </p>
        </>
      )
    },
    {
      id: 2,
      pseudo: "Sune'emon Torii",
      name: 'Jeremie Evequoz',
      src: Profile2,
      twitter: 'jayzhvj_eth',
      instagram: 'jeremie_evequoz',
      linkedin: 'jérémie-evéquoz-7a4547134',
      title: 'Co-founder',
      description: (
        <>
          <p>
            My name is Jérémie ! I&apos;m 28 years old and I&apos;m from Sion,
            Switzerland
          </p>

          <p>
            I&apos;ve been working in computer sciences for about 10 years,
            mostly system and network oriented and also been working with
            @Uesugi Kenshin for the last 3 years. I&apos;ve been familiar with
            crypto since 2016 (I was not as involved as I am now).
          </p>

          <p>
            In 2015 I spent a year abroad in Queenstown, New Zealand and
            that&apos;s where I met @Kyosuke Rogue. By the way the best burgers
            ever are in QT without any doubt. 🍔
          </p>

          <p>
            Since I live in the middle of the Alps I&apos;ve been skiing a lot
            since my very young age. I participated to a lot of competition and
            then started to train younger ones. ⛷️ It&apos;s in 2014 that I met
            @Ibaraki Tsukasa since then it&apos;s been a pretty close friend and
            a not so bad gaming partner 🎮
          </p>
        </>
      )
    },
    {
      id: 3,
      pseudo: 'Ibaraki Tsukasa',
      name: 'Alexandre Le Corre',
      src: Profile4,
      instagram: '_elreco',
      linkedin: 'alexandre-le-corre',
      title: 'Developer',
      description: (
        <>
          <p>
            I&apos;m Alexandre and I&apos;m 28 years old. I work as a lead
            developer in a Parisian start-up. 💻
          </p>

          <p>
            In my work I always value the human rather than the technical
            skills.
          </p>
          <p> For me, a good atmosphere at work is essential. 🧑‍🤝‍🧑</p>
          <p>I really like working from home. 🏠</p>

          <p>
            I love racket sports like table tennis, tennis, badminton. 🎾 By the
            way I pay a McDo to anyone who beats me at Tennis.
          </p>
        </>
      )
    },
    {
      id: 4,
      pseudo: 'Uesugi Kenshin',
      name: 'Davide Mendes',
      src: Profile5,
      twitter: 'dragorath_eth',
      linkedin: 'davide-mendes',
      title: 'Developer',
      description: (
        <>
          <p>Hello everyone!</p>

          <p>
            My name is Davide ! I&apos;m from Portugal and I live in
            Switzerland.
          </p>
          <p>
            I&apos;m a computer engineer who loves to be on the edge with new
            technologies 💻, that so the blockchain interests me.
          </p>

          <p>I like to stay in movement and to be human. 🤟🏼</p>
        </>
      )
    },
    {
      id: 5,
      pseudo: 'Nephophiley',
      name: 'Tita Carella',
      src: Profile6,
      twitter: 'titacarella',
      title: 'Artist',
      description: (
        <>
          <p>
            My name is Tita and I&apos;m a 21 years old computer science
            engineering student since 2018. 💻
          </p>
          <p>
            I live in Bekasi, Indonesia. I started to draw at 7 and like to
            explore many art genres. basically I like to learn many things
            beside drawing. 👩‍🎨
          </p>

          <p>
            I&apos;m still new with NFT but it got my interest and seems fun to
            me.
          </p>

          <p>
            I usually play games and watch some movies or anime when
            there&apos;s nothing do.
          </p>
        </>
      )
    }
  ]
```
