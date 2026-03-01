# 3. Apply PCA (Full Components)
pca_full = PCA()
pca_full.fit(X_scaled)

# 4. Calculate Cumulative Variance
# This tells us: "If we keep N components, how much original data do we preserve?"
cumulative_variance = np.cumsum(pca_full.explained_variance_ratio_)

# 5. Plot Cumulative Variance
plt.figure(figsize=(10, 6))
plt.plot(cumulative_variance, linewidth=2, color='blue')
plt.xlabel('Number of Components')
plt.ylabel('Cumulative Explained Variance')
plt.title('PCA Explained Variance Ratio')
plt.grid(True)

# Add a line at 95% variance
plt.axhline(y=0.95, color='r', linestyle='--', label='95% Variance Threshold')
plt.legend(loc='best')
plt.show()

# Find exact components needed for 95%
n_components_95 = np.argmax(cumulative_variance >= 0.95) + 1
print(f"Number of components needed to keep 95% variance: {n_components_95}")
print(f"Compression: Reduced features from 64 to {n_components_95}")
