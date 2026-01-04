# MLB Player Performance Projection System

A comprehensive machine learning system for projecting MLB player performance, similar to industry-standard projection systems like STEAMER, ZiPS, and PECOTA used by professional teams.

## 📊 Project Overview

This project develops a data-driven player projection system that forecasts future performance metrics based on historical batting statistics. The system helps MLB front offices make informed decisions about:

- **Free Agency**: Identifying undervalued breakout candidates
- **Trade Decisions**: Recognizing players at risk of decline
- **Roster Management**: Optimizing lineup construction and playing time allocation
- **Contract Negotiations**: Providing objective performance forecasts

## 🎯 Key Features

- **Historical Analysis**: 25 years of MLB batting data (2000-2024)
- **Advanced Metrics**: OPS, WAR estimates, and sabermetric calculations
- **Machine Learning Models**: Multiple model comparison and selection
- **Projection Engine**: 2025 season performance forecasts
- **Business Intelligence**: Actionable insights for front office decision-making
- **Player Clustering**: Categorization into breakout candidates and decline risks

## 📁 Project Structure

```
mlb-player-projection/
├── notebooks/
│   ├── 01_data_preparation.ipynb       # Data loading and preprocessing
│   ├── 02_exploratory_analysis.ipynb   # Statistical analysis and visualization
│   ├── 03_modeling.ipynb               # Model development and evaluation
│   └── 04_projection_system.ipynb      # Production system and insights
├── data/
│   └── batting_with_projections.csv    # Processed dataset
├── models/                              # Trained model artifacts
├── reports/                             # Generated projections and reports
└── README.md
```

## 📈 Dataset

**Source**: Lahman Baseball Database  
**Records**: 5,157 player-seasons  
**Players**: 1,157 unique players  
**Time Period**: 2000-2024  
**Features**: 33 variables including traditional stats and advanced metrics

### Key Variables

- **Traditional Stats**: AVG, HR, RBI, SB, BB, SO
- **Advanced Metrics**: OPS, OBP, SLG
- **Career Metrics**: Cumulative games, plate appearances, home runs
- **Target Variables**: Next season performance (OPS_next, HR_next, etc.)
- **Derived Features**: Age groups, years of experience, player aging curves

## 🔧 Technical Stack

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **scikit-learn**: Machine learning models
- **matplotlib/seaborn**: Data visualization
- **numpy**: Numerical computations

## 📓 Notebook Workflow

### 1. Data Preparation (`01_data_preparation.ipynb`)

- Load Lahman Baseball Database
- Calculate advanced metrics (OPS, estimated WAR)
- Create year-to-year performance datasets
- Filter to qualified players (minimum playing time)
- Generate features for modeling

### 2. Exploratory Analysis (`02_exploratory_analysis.ipynb`)

- Analyze performance distributions and trends
- Examine aging curves and career trajectories
- Identify correlations between metrics
- Visualize key patterns in player development
- Study position-specific performance characteristics

### 3. Modeling (`03_modeling.ipynb`)

- Engineer predictive features from historical data
- Train multiple machine learning models:
  - Linear Regression
  - Ridge Regression
  - Random Forest
  - Gradient Boosting
- Evaluate model performance (RMSE, MAE, R²)
- Analyze feature importance
- Select best model for deployment

### 4. Projection System (`04_projection_system.ipynb`)

- Generate 2025 season performance forecasts
- Identify breakout candidates (young players with upside)
- Flag decline risk players (veterans likely to underperform)
- Create player comparison tools
- Export projections for team use
- Provide strategic recommendations

## 🎯 Key Insights

### Breakout Candidates

Young players (under 27) projected to significantly improve performance:

- Minimum 50-point OPS increase projected
- High upside for roster construction
- Potential market inefficiencies for free agency

### Decline Risk

Veteran players (30+) projected to experience performance drop:

- 30+ point OPS decrease expected
- Important for contract decisions
- Trade deadline considerations

### Strategic Recommendations

1. **Invest in Youth**: Target undervalued young talent with projection upside
2. **Manage Risk**: Avoid overcommitting to declining veterans
3. **Market Inefficiencies**: Focus on players the market undervalues
4. **Portfolio Approach**: Balance proven performance with high-upside prospects

## 📊 Model Performance

The final model achieves:

- **Accuracy**: Competitive with industry-standard projection systems
- **Feature Importance**: Age, recent performance, and career trajectory are key predictors
- **Validation**: Tested on holdout seasons to ensure generalization

## 🚀 Usage

### Running the Analysis

1. **Data Preparation**

   ```bash
   jupyter notebook 01_data_preparation.ipynb
   ```

2. **Exploratory Analysis**

   ```bash
   jupyter notebook 02_exploratory_analysis.ipynb
   ```

3. **Model Training**

   ```bash
   jupyter notebook 03_modeling.ipynb
   ```

4. **Generate Projections**
   ```bash
   jupyter notebook 04_projection_system.ipynb
   ```

### Output Files

The system generates:

- `2025_player_projections.csv`: Complete projection report with categories
- Model artifacts in `models/` directory
- Visualization outputs in notebook cells

## 📋 Requirements

```python
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## 🎓 Methodology

The projection system uses:

1. **Historical Performance**: 3-5 year lookback windows
2. **Aging Curves**: Age-adjusted expectations
3. **Regression to Mean**: Statistical correction for outliers
4. **Playing Time Filters**: Minimum AB/PA thresholds
5. **Feature Engineering**: Derived metrics and interaction terms

## 📊 Business Applications

### Front Office Use Cases

- **Free Agent Evaluation**: Identify market inefficiencies
- **Trade Analysis**: Assess value of players in deals
- **Arbitration**: Provide objective performance forecasts
- **Draft Strategy**: Compare professional prospects
- **Salary Cap Management**: Project future value

### Analyst Use Cases

- **Content Creation**: Data-driven player profiles
- **Fantasy Baseball**: Projection-based rankings
- **Research**: Testing hypotheses about player development

## 🔮 Future Enhancements

Potential improvements:

- [ ] Incorporate injury history and durability metrics
- [ ] Add defensive metrics (UZR, DRS)
- [ ] Pitcher performance projections
- [ ] Park factor adjustments
- [ ] Minor league translation algorithms
- [ ] Real-time API integration
- [ ] Interactive dashboard deployment

## 👤 Author

**Yunjae Jung**  
MLB Player Performance Projection System  
January 2026

## 📄 License

This project is for educational and research purposes.

## 🙏 Acknowledgments

- **Lahman Baseball Database**: Historical baseball statistics
- **Sabermetric Community**: Methodological foundations
- **MLB Teams**: Industry-standard projection systems (STEAMER, ZiPS, PECOTA)

## 📞 Contact

For questions or collaboration opportunities, please reach out through the project repository.

---

_This projection system is designed for educational and analytical purposes. Professional MLB teams use more sophisticated systems with additional proprietary data sources._
