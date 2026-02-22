# Temperature Sensor Data Simulator with Noise & Cleaning 🌡️🔧

A complete **sensor data simulation project** for industrial environments. I created a synthetic temperature dataset, intentionally added **missing values** and **noise**, then cleaned it and built ML models. Perfect for testing **data preprocessing techniques** and **machine learning pipelines**!

## 🔥 What Makes This Project Special?
- ✅ **Custom Dataset Creation** — Simulated real-world temperature sensor data
- ✅ **Missing Values Injection** — Intentionally removed data points
- ✅ **Noise Addition** — Added realistic sensor noise
- ✅ **Data Cleaning** — Fixed missing values and denoised the signal
- ✅ **ML Models** — Built prediction models (users can choose their own!)
- ✅ **Hardware Ready** — Compatible with **USB to Serial RS485 converters** (noise-free data collection)

## 🏭 Real-World Application
This project simulates what happens in **factories**:
1. Sensors collect temperature data
2. Data gets corrupted (missing values, noise)
3. Engineers clean and analyze it
4. ML models predict future temperatures

## 🧠 What I Did

### 1. **Created Synthetic Dataset**
   - Simulated temperature readings over time
   - Added realistic patterns (daily cycles, trends)

### 2. **Added Missing Values**
   ```python
   # Randomly remove 10% of data
   df.loc[random_sample, 'temperature'] = np.nan
   ```

### 3. **Added Noise**
   ```python
   # Add Gaussian noise
   noise = np.random.normal(0, 0.5, len(df))
   df['noisy_temp'] = df['temperature'] + noise
   ```

### 4. **Cleaned Everything**
   - **Missing values:** Interpolation, forward fill
   - **Noise:** Moving average, low-pass filters
   - **Outliers:** IQR method

### 5. **Built ML Models**
   - Linear Regression (baseline)
   - Deep Learning (LSTM for time series)
   - Users can choose their own!

### Option 3: **Connect to Real Hardware**
> 💡 **Pro Tip:** Use **USB to Serial RS485 converters** for real sensor data collection — they provide noise-free transmission!

## 📊 Dataset Features
- **Timestamp:** Time of reading
- **Temperature:** Actual temperature (°C)
- **Noisy_Temperature:** Temperature + noise
- **Missing_Flag:** Indicates if value was missing
- **Cleaned_Temperature:** After preprocessing

## 🎯 Why This Project Matters
- ✅ **Learn Data Preprocessing** — Missing values, noise, outliers
- ✅ **Understand Sensor Data** — Real-world industrial applications
- ✅ **Compare ML Models** — Linear vs Deep Learning
- ✅ **Hardware Integration** — RS485 converters for real data


## 🔮 Future Improvements
- [ ] Add more sensor types (humidity, pressure)
- [ ] Real-time data simulation

## 📧 Contact
Built by Omid Bagheri — simulating real-world data challenges for better ML!

## 🙏 Hardware Note
For real sensor data collection, consider using **USB to Serial RS485 converters** — they provide stable, noise-free communication with industrial sensors!