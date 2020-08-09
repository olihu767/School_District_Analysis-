# School_District_Analysis-

Background
The grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent of this academic dishonesty, they want to uphold the standards of state testing and have turned to you for help.

After assessing the situation with the school superintendent and Maria, you decide the best approach is to:

Replace the ninth-grade math and reading scores from Thomas High School.
Keep all other data associated with the ninth-grade students and Thomas High School intact.

## Objectives
The goals of this challenge are for you to:

Filter DataFrames using logical operators.
Replace the incorrect values with NaN.
Explain how your PyCitySchools analysis changes after you handle the incorrect data.  

## Resources
* Data Source: schools_complete.csv, students_complete.csv
* Software: Python 3.7.6, Jupyter Notebook 6.0.1

## Method
To compare the results between these changes:

1. We created a duplicate notebook to conduct the changes.
2. Corrected the students' names so there are no professional prefixes or suffixes.
3. Replace the reading and math scores for ninth graders at Thomas High School with NaN.
- Use loc on the student_data_df DataFrame to select the columns by condition.
- Set the column you want equal to 'NaN' by using np.nan for the reading and math scores separately.
- In order to use np.nan, you will need to import Numpy.
4. Your code to do step 3 will look like the following:
 student_data_df.loc[(student_data_df['grade'] == '9th') & (student_data_df['school_name'] == 'Thomas High School'), ['reading_score', 'math_score']] = np.nan
5. Merge the clean student data with the school dataset.
