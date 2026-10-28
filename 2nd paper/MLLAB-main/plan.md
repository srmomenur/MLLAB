
# শিক্ষার্থী মানসিক চাপ পূর্বাভাস: সম্পূর্ণ গবেষণা নোটবুক

এই master notebook-এ ডেটা অডিট থেকে শুরু করে baseline evaluation, domain-level ablation, holdout evaluation, SHAP ব্যাখ্যা, robustness summary এবং hypothetical what-if analysis পর্যন্ত পুরো workflow রাখা হয়েছে।

**গুরুত্বপূর্ণ নিয়ম**

- Python code, variable names, function names, plot labels এবং output text ইংরেজিতে রাখা হয়েছে।
- Code cell-এর `#` comments বাংলায় লেখা হয়েছে।
- Markdown cell বাংলায় লেখা হয়েছে।
- `stress_level`-এর class labels 0, 1, 2-কে low, medium, high হিসেবে ধরা হবে না, যতক্ষণ না dataset documentation দিয়ে তা নিশ্চিত করা যায়।
- Domain mapping feature name-এর semantic interpretation; এটি dataset creator-এর official mapping বলে দাবি করা হচ্ছে না।
- Model-based what-if analysis association বা causation প্রমাণ করে না।


## গবেষণা পরিকল্পনা

১. ডেটা অডিট
২. Feature-to-domain mapping এবং validation
৩. Stratified 80/20 train-holdout split
৪. তিনটি baseline model-এর 5-fold cross-validation, তিনটি seed-এ
৫. Holdout set-এ নির্বাচিত model-এর একবারের final evaluation
৬. Domain-removal এবং single-domain-only ablation
৭. SHAP global ও class-wise explanation এবং domain aggregation
৮. Robustness summary এবং সীমাবদ্ধতা
৯. Hypothetical what-if sensitivity analysis

সব model selection এবং ablation comparison training data-এর cross-validation-এর ওপর নির্ভর করবে। Holdout set hyperparameter tuning বা feature selection-এর জন্য ব্যবহার করা হবে না।
