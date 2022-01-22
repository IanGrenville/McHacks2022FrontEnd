<script type="module">
import * as Plot from "https://cdn.skypack.dev/@observablehq/plot@0.4";
data = FileAttachment("fake_data.csv").csv({typed: true})
document.body.appendChild(
  Plot.plot({
  marks: [
    Plot.ruleX([0]),
    Plot.barX(data, {x: "Player", y: "Percentage Negative Sentiment"})
  ]
}));
</script>



# NBHate: Estimating The Level of Vitriol Surrounding Famous Athletes

NBHate is an open-source data-driven machine learning and data analysis project created by Ian Grenville and Tayseer Chowdhury for the McHacks 2022 hackathon.

The project reads public opinion by extracting recent posts featuring an athletes name on Twitter.com and passing them through a SentimentNet neural network model, and using the models inferences sentence sentiment/polarity we determine which names are most frequently co-occuring with negative sentiment. This information is then exported and visualized using the Observable Plot library. 
