### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 30.09.2025
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python
df = pd.read_csv('clustervisitor.csv')
print(df)
cluster = {"Young": (df['Age'] <= 30), "Middle": ((df['Age'] > 30) & (df['Age'] <= 50)), "Old": (df['Age'] > 50)}
count = []
for g, c in cluster.items():
  visitors = df[c]
  count.append(len(visitors))
  print(f"Visitors in {g} Group")
  print(visitors)
  print(count)
```
### Output:
<img width="498" height="692" alt="Screenshot 2025-09-22 at 3 55 40 PM" src="https://github.com/user-attachments/assets/77123db1-4425-43a0-a2cf-d6a69a6af4ec" />

### Visualization:
```python
plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()

plt.scatter(df5['Age'], df5['Salary'], c=df5['cluster'])
plt.xlabel('Age')
plt.ylabel('Salary')
plt.title('Clusters')
plt.show()
```
### Output:

<img width="833" height="561" alt="Screenshot 2025-09-22 at 3 55 56 PM" src="https://github.com/user-attachments/assets/afbd2836-7103-4283-b022-e304f2296a61" />
<img width="652" height="466" alt="Screenshot 2025-09-22 at 3 56 10 PM" src="https://github.com/user-attachments/assets/1e702e06-9c76-40ba-ab30-56a5bc66defc" />

### Result:
The implement Cluster and Visitor Segmentation for Navigation patterns in Python is execute successfully
