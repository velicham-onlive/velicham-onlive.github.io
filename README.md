# Velicham Quran Dars-Podcast conversion

#### What? (The Idea):
The conversion of WhatsApp-based audio classes to podcast series. The series was called **Velicham Quran Dars series** and running in multiple batches within the Malayalee Mulsim communities globally.

#### Why? (The step forward):
The Velicham series had already been grown to multiple batches and still growing, hence to cater the series with it's full potential the Team Velicham decided to introduce the same thru podcast services to benefit the communities in an organized fashion. Meanwhile, the podcasts are gaining momentum in the current world due to an organised way for delivering the series of audio content to the public. Recent support from multiple vendors, especially from Google, endorsed the same to gain momentum in the Eastern world.

#### How? (The solution):
The Google podcast [guide](https://developers.google.com/search/docs/data-types/podcast) made the podcasts searchable globally for the different podcast engines catering in the Mobile and other platforms.

#### The implementation approach (proposal):
As per documentation the audio files (the podcast episodes) to be hosted in public servers, we opted GitHub, with certain tags and an index page to reach out by Googlebot or similar ones. The index.html points to the feeds(\*.rss) file where all podcasts are described with possible details, in turn, it points to an absolute path of the audio files.

## Contributing

We opted the open-source platform to welcome your thoughts on the projects. If you'd like to contribute, please take a look at the [issues](https://github.com/velicham-onlive/velicham-onlive.github.io/issues) and create one if your idea/issue is not found in the list.

#### Who can contribute:
Anyone who are willing to volunteer can contribute in this effort, please refer our [Code of Conduct](https://github.com/velicham-onlive/velicham-onlive.github.io/blob/master/CODE_OF_CONDUCT.md).
We use Git as VCS and follow [GitHubFlow](https://guides.github.com/introduction/flow/) process model for review and branch management.

#### How to contribute: ## Contributing [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/velicham-onlive/velicham-onlive.github.io/issues)

- Take up an issue/feature from the [issues](https://github.com/velicham-onlive/velicham-onlive.github.io/issues) by assigning self.
- Commit intended code changes to relevant/new branch.
- Once completed, create Pull-request and assign reviewers.

#### What to commit:
As you might notice, the podcast episodes are already layed out and it's available in iTunes, Google and other podcasts engines. Need volunterely contribution in introducing new episodes in the feed file ([podcast.rss](https://github.com/velicham-onlive/velicham-onlive.github.io/blob/master/podcast.rss)) by appending in the below format.

```xml
<item>
  <title>46.സൂറ ഇഖ്‌ലാസ് - ആയത്ത് 4</title>
  <description>
    <![CDATA[<p>Velicham Qur'an Dars series</p><p>ഖുർആൻ ക്ലാസ് #46</p><p>💠Surah Al-Iklas💠<br />ആയത്ത്-4</p><p>وَلَمْ يَكُن لَّهُۥ كُفُوًا أَحَدٌۢ <br /> അവനു തുല്യനായി ആരുമില്ല.</p><p>🔸Admin Team Onlive🔸</p>]]>
  </description>
  <enclosure url="https://velicham-onlive.github.io/audios/112-ikhlaas/8-vqd-podcast-unit112.m4a" type="audio/m4a" length="708000"/>
  <itunes:duration>06:52</itunes:duration>
  <pubDate>Thursday, 25 Apr ‎2019 ‏‎12:00:00 GMT</pubDate>
  <guid>8-vqd-podcast-unit112</guid>
</item>
```

- **&lt;item&gt;** : A podcast episode will be furnished with this tag.
- **&lt;title&gt;** : The name of the episode, will be in Malayalam locale.
- **&lt;description&gt;** : The description about the episode with possible details. It might contain multiple locale hence it is recommended to be wrapped with CDATA.
- **&lt;enclosure&gt;** : points to the fully-qualified URL of the episode audio file with audio type and audio length in bytes.
- **&lt;itunes:duration&gt;** : audio duration in mm:ss format.
- **&lt;pubDate&gt;** : publication date of the episode.
- **&lt;guid&gt;** : A permanently-assigned, case-sensitive Globally Unique Identifier for a podcast episode. Should be unique and unchanging over time, scoped to this podcast. GUIDs are compared to indicate which episodes are new.
  
