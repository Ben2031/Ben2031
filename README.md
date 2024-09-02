import matplotlib.pyplot as plt


languages = ['Java', 'Python', 'PHP', 'JavaScript', 'C#', 'C++']
popularity = [22.2, 19.6, 8.8, 8.0, 7.7, 6.7]


plt.figure(figsize=(10, 6))  

bars = plt.bar(languages, popularity, color='skyblue')
plt.title('Popularity of Programming Languages', fontsize=20)
plt.xlabel('Programming Languages', fontsize=12)
plt.ylabel('Popularity (%)', fontsize=12)
plt.xticks(rotation=45)
plt.ylim(0, 25) 
for bar in bars:
    height = bar.get_height()
    plt.text(bar.get_x() + bar.get_width() / 2.0, height + 0.5, f'{height}%', 
             ha='center', va='bottom', fontsize=10)
plt.tight_layout()  
plt.show()
