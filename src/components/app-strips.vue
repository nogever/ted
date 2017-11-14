<template>
  <div class="strips">
    <div v-for="strip in strips" class="strip">
      <button></button>
      <div>
        <h2>{{ strip.name }}</h2>
        <ul>
          <li v-for="item in strip.list" class="item">
            <router-link to="/video">
              <div class="item-image" v-bind:style="{ backgroundImage: `url(${item.backgroundUrl})` }">
                <div class="timestamp">{{ item.timestamp }}</div>
              </div>
              <div class="item-title">{{ item.title }}</div>
            </router-link>
          </li>
        </ul>
      </div>
      <button></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app-strips',
  data: () => ({
    strips: [
      {
        name: 'Newest Talks',
        list: [
          {
            timestamp: '12:23',
            title: `What I learned serving time for a crime I didn't commit`,
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/87977bdd-8faf-4a5a-9ac4-118d31e7e532/TeresaNjoroge_2017W-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '16:03',
            title: 'How judges can show respect',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/599c410d-ff8b-4028-8397-7df1494093df/VictoriaPratt_2017S-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '17:10',
            title: 'The biggest risks facing cities—and some solutions',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/93a89e02-72b0-4a82-a77d-41506ee7e315/RobertMuggah_2017G-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '10:54',
            title: 'We should aim for perfection—and stop fearing failure',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/9edf62ef-2366-4276-8e71-93c42af15b48/JonBowers_2017S-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '18:50',
            title: `An interview with Mauritius's first female president`,
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/51c2ac90-8d81-4e1d-b786-caf8e3a3c21d/AmeenahGuribFakim_2017G-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '14:11',
            title: 'Why wildfires have gotten worse—and what we can do about it',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/fdc20ea0-fdf1-4e31-a2d1-a89bfc4d77be/PaulHessburg_2017X-embed.jpg?quality=63&w=512'
          }
        ]
      },
      {
        name: 'Trending',
        list: [
          {
            timestamp: '7:53',
            title: `Alzheimer's is not normal aging — and we can cure it`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/621f9027fc1cc0c16483d6cb752bc2d9ed9b81a3_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '7:20',
            title: 'The day I stood up alone',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/c503844ad499db8826d41e0b5bc5df56bd375d22_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '13:03',
            title: 'How I use sonar to navigate the world',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/9d9e218a26b00bd5a0eb2f69f9a44e768fdebc26_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '20:34',
            title: 'Can we create new senses for humans?',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1efebe64a094b2ee95cd62eec52ddf2238a92510_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '25:00',
            title: `Why giving away our wealth has been the most satisfying thing we've done`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1c443a121cbd80555dd1cf7389359b5050786e07_1600x1200.jpg?quality=63&w=512'
          },
          {
            timestamp: '8:04',
            title: 'Image recognition that triggers augmented reality',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/22a286b5117b23672b44baf155695c4ca12eb981_1600x1200.jpg?quality=63&w=512'
          }
        ]
      },
      {
        name: 'Recommended today',
        list: [
          {
            timestamp: '12:23',
            title: `What I learned serving time for a crime I didn't commit`,
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/87977bdd-8faf-4a5a-9ac4-118d31e7e532/TeresaNjoroge_2017W-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '16:03',
            title: 'How judges can show respect',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/599c410d-ff8b-4028-8397-7df1494093df/VictoriaPratt_2017S-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '17:10',
            title: 'The biggest risks facing cities—and some solutions',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/93a89e02-72b0-4a82-a77d-41506ee7e315/RobertMuggah_2017G-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '10:54',
            title: 'We should aim for perfection—and stop fearing failure',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/9edf62ef-2366-4276-8e71-93c42af15b48/JonBowers_2017S-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '18:50',
            title: `An interview with Mauritius's first female president`,
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/51c2ac90-8d81-4e1d-b786-caf8e3a3c21d/AmeenahGuribFakim_2017G-embed.jpg?quality=63&w=512'
          },
          {
            timestamp: '14:11',
            title: 'Why wildfires have gotten worse—and what we can do about it',
            backgroundUrl: 'https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/fdc20ea0-fdf1-4e31-a2d1-a89bfc4d77be/PaulHessburg_2017X-embed.jpg?quality=63&w=512'
          }
        ]
      },
      {
        name: 'Heard on TED radio hour',
        list: [
          {
            timestamp: '7:53',
            title: `Alzheimer's is not normal aging — and we can cure it`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/621f9027fc1cc0c16483d6cb752bc2d9ed9b81a3_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '7:20',
            title: 'The day I stood up alone',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/c503844ad499db8826d41e0b5bc5df56bd375d22_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '13:03',
            title: 'How I use sonar to navigate the world',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/9d9e218a26b00bd5a0eb2f69f9a44e768fdebc26_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '20:34',
            title: 'Can we create new senses for humans?',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1efebe64a094b2ee95cd62eec52ddf2238a92510_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '25:00',
            title: `Why giving away our wealth has been the most satisfying thing we've done`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1c443a121cbd80555dd1cf7389359b5050786e07_1600x1200.jpg?quality=63&w=512'
          },
          {
            timestamp: '8:04',
            title: 'Image recognition that triggers augmented reality',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/22a286b5117b23672b44baf155695c4ca12eb981_1600x1200.jpg?quality=63&w=512'
          }
        ]
      },
      {
        name: 'Tech-driven innovation',
        list: [
          {
            timestamp: '7:53',
            title: `Alzheimer's is not normal aging — and we can cure it`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/621f9027fc1cc0c16483d6cb752bc2d9ed9b81a3_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '7:20',
            title: 'The day I stood up alone',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/c503844ad499db8826d41e0b5bc5df56bd375d22_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '13:03',
            title: 'How I use sonar to navigate the world',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/9d9e218a26b00bd5a0eb2f69f9a44e768fdebc26_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '20:34',
            title: 'Can we create new senses for humans?',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1efebe64a094b2ee95cd62eec52ddf2238a92510_2880x1620.jpg?quality=63&w=512'
          },
          {
            timestamp: '25:00',
            title: `Why giving away our wealth has been the most satisfying thing we've done`,
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/1c443a121cbd80555dd1cf7389359b5050786e07_1600x1200.jpg?quality=63&w=512'
          },
          {
            timestamp: '8:04',
            title: 'Image recognition that triggers augmented reality',
            backgroundUrl: 'https://pi.tedcdn.com/r/pe.tedcdn.com/images/ted/22a286b5117b23672b44baf155695c4ca12eb981_1600x1200.jpg?quality=63&w=512'
          }
        ]
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
.strips {
  display: flex;
  flex-direction: column;
  align-items: center;
  .strip {
    width: 100%;
    max-width: 1200px;
    display: flex;
    align-items: center;
    margin: 10px 0;
    h2 {
      background: #E62B1E;
      color: white;
      display: inline-block;
      padding: 6px 10px;
      font-size: 12px;
      text-transform: uppercase;
      margin-bottom: 2px;
    }
    ul {
      display: flex;
      .item {
        width: 190px;
        background: white;
        border: 1px solid #eee;
        margin-right: 8px;
        cursor: pointer;
        .item-image {
          height: 110px;
          background-size: cover;
          position: relative;
          margin: -1px;
          z-index: 0;
          .timestamp {
            position: absolute;
            right: 6px;
            bottom: 6px;
            color: white;
            background: black;
            border-radius: 2px;
            padding: 2px 6px;
            font-size: 12px;
          }
        }
        .item-title {
          padding: 6px;
          font-size: 16px;
          font-weight: 700;
        }
        &:hover {
          opacity: .85;
        }
      }
    }
  }
}
</style>
