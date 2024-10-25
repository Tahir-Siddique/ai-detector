# AI Content Detector

A lightweight, browser-based tool for analyzing text to identify potential AI-generated content. This tool uses multiple heuristic approaches to evaluate text and provide a comprehensive analysis of its characteristics.

## 📝 Features

- **No Dependencies**: Pure HTML, CSS, and JavaScript implementation
- **Browser-Based**: Runs entirely in the client's browser
- **Real-Time Analysis**: Instant feedback as users input text
- **Multiple Metrics**: Analyzes text across various dimensions
- **Responsive Design**: Works on both desktop and mobile devices
- **Privacy-Focused**: No data sent to external servers

## 🚀 Quick Start

1. Clone this repository:
```bash
git clone https://github.com/Tahir-Siddique/ai-detector.git
```

2. Open `index.html` in your web browser
3. Paste text into the input area
4. Click "Analyze Text" to see results

## 💡 How It Works

The detector analyzes text using four primary metrics:

### 1. Repetitiveness Score (30% weight)
Measures the frequency of repeated words and phrases. AI-generated content often shows patterns of repetition.

```javascript
// Example of how repetitiveness is calculated
const repetitionScore = uniqueWords / totalWords * 100;
```

### 2. Naturalness Score (30% weight)
Evaluates sentence structure variation and length distribution.
- Checks sentence length variety
- Analyzes sentence structure patterns
- Identifies unusual uniformity

### 3. Structural Patterns (20% weight)
Examines paragraph organization and formatting:
- Paragraph length variation
- Text organization patterns
- Overall document structure

### 4. Vocabulary Diversity (20% weight)
Assesses the richness and variety of language used:
- Unique words ratio
- Word complexity distribution
- Vocabulary range

## 📊 Understanding Results

The tool provides scores in several categories:

| Score Range | Interpretation |
|-------------|----------------|
| 70-100% | Likely Human-Written |
| 40-70%  | Uncertain |
| 0-40%   | Potentially AI-Generated |

### Sample Output
```json
{
    "overallScore": 85.5,
    "metrics": {
        "repetitiveness": 90.2,
        "naturalness": 85.7,
        "structuralPatterns": 78.9,
        "vocabularyDiversity": 82.4
    }
}
```

## ⚠️ Limitations

- **Not Definitive**: This tool provides indicators, not absolute determinations
- **False Positives**: Human-written content may sometimes be flagged
- **False Negatives**: Sophisticated AI content might pass undetected
- **Length Requirement**: Requires minimum 50 characters for meaningful analysis
- **Language**: Currently optimized for English text only

## 🛠 Customization

### Adjusting Weights

You can modify the importance of each metric by adjusting the weights in the `calculateOverallScore` function:

```javascript
const weights = {
    repetitiveness: 0.3,    // 30%
    naturalness: 0.3,       // 30%
    structuralPatterns: 0.2, // 20%
    vocabularyDiversity: 0.2 // 20%
};
```

### Styling

The tool uses a simple CSS framework that can be customized in the `<style>` section of the HTML file.

## 🌟 Future Improvements

- [ ] Add support for multiple languages
- [ ] Implement more sophisticated text analysis algorithms
- [ ] Add export functionality for results
- [ ] Include historical analysis tracking
- [ ] Add batch processing capabilities

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add some amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📞 Support

If you have any questions or need support:
1. Open an issue in the repository
2. Check existing documentation
3. Review closed issues for similar problems

---

**Note**: This detector is intended as a supplementary tool and should not be used as the sole method for determining whether content is AI-generated. Results should be interpreted alongside other factors and human judgment.
