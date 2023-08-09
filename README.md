# Italian Ham Radio Repeaters Data Manipulation

In this project, we worked on manipulating and cleaning data related to radio frequencies.

## Steps Undertaken:

1. **Initial Data Import**: Started by importing the data from ik2ane.it "ponti" list which contained frequency data.
2. **Data Transformation**:
   - Created a new column `tx_freq` which applied a frequency shift based on the `shift` column.
   - Renamed the `freq` column to `rx_freq`.
3. **Data Export**: Formatted the data to match a template file (`Centro Nord 4.0.csv`). This involved:
   - Renaming columns.
   - Mapping values from the original dataframe to the format needed in the template.
   - Adding new columns as required by the template.
4. **Channel Numbering**: Added a new column to sequentially number the channels.
5. **Frequency Shift Handling**: Modified the handling of frequency shifts to match a template, considering MHz and KHz shifts.
6. **Mode Mapping**: Mapped the `grp` column from the original dataframe to the `Operating Mode` in the new dataframe.
7. **Tone Mapping**: Mapped the `tono` column to derive the `Tone Mode` and `CTCSS` columns.
8. **Location and Name Creation**: Derived the province based on the `località` column and created a new name by combining `nome`, province, and `località`.
9. **Data Sorting**: Sorted the dataframe based on distance to a given QTH using the Maidenhead Grid Square system.
10. **Data Filtering**: Dropped rows based on certain criteria, such as `freq` values being greater than a specific threshold.

## Libraries Used:

- **Pandas**: For data manipulation and transformation.
- **Maidenhead**: For conversion between Maidenhead grid squares and latitude/longitude coordinates.
