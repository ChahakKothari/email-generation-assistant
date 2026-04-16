# Email Generation Assistant

## Setup & How to Run
1. Open `email_generator (1).ipynb` in Google Colab
2. Run first cell: `!pip install groq pandas`
3. Replace `"your-api-key-here"` with your Groq API key
4. Run all cells in order

## Files
- `email_generator (1).ipynb` - Main notebook
- `evaluation_results.csv` - Model A evaluation scores
- `model_comparison.csv` - Model A vs Model B comparison

## Prompting Technique
**Few-Shot Prompting** — Model A uses 2 examples before generating.
Model B uses Zero-Shot (no examples) for comparison.

## Custom Metrics
| Metric | Description |
|--------|-------------|
| Fact Recall | Checks how many input facts appear in email |
| Tone Score | LLM-as-a-Judge rates tone match (0-1) |
| Format Score | Checks Subject, greeting, closing present |

## Results
| Model | Strategy | Avg Score |
|-------|----------|-----------|
| Model A | Few-Shot | 0.57 |
| Model B | Zero-Shot | 0.66 |

## Model Used
Llama 3.1 8B via Groq API
