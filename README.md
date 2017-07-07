# Overview of Content:



### mlo_00_run_all:

Newest Data will be downloaded / imported by default. This option can be changed in: __mlo_01_import.ipynb__

Run every single notebook:
- mlo_01_import.ipynb
- mlo_02_merge_data.ipynb
- mlo_03_plot.ipynb
- mlo_04_correlations.ipynb
- mlo_05_fft.ipynb
- mlo_06-1_filter_mmlo.ipynb
- mlo_06-2_filter_oeni.ipynb
- mlo_07_filtered_correlations_fft.ipynb
- mlo_08_spectra_analysis.ipynb
- mlo_09_synth_trend_prediction.ipynb



### mlo_01_import:


__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Import / Download Data
- Create Subfolders if they do not exists
- Mauna Loa Data (monthly mean)
- ONI-Data (Oceanic Nino Index)


__Save Dataframes as Notebook Variables and as Text Files__:
- Mauna Loa Data (monthly mean):
    - mmlo
    - eq_trend_mmlo
    - p_trend_mmlo
- ONI-Data (Oceanic Nino Index):
    - oeni
    - eq_trend_oeni
    

### mlo_02_merge_data:


__Sections__:
- Main Module Import Section and Notebook Settings
- Read Notebook Variables
- Merge and Store Time Series


__Save Dataframes as Notebook Variables and as Text Files__:
- Merge and Store Time Series:
    - full_a
    - cut_a


### mlo_03_plot:


__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Maua Loa Time Series
- ONI Time Series

    
__Plot and Save Figures__:
- Maua Loa Time Series:
    - raw_mmlo.pdf
    - trend_mmlo.pdf
    - notrend_mmlo.pdf
- ONI Time Series:
    - raw_oeni.pdf
    
    
### mlo_04_correlations:


__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Mauna Loa Auto-Correlation
- ONI Auto-Correlation
- Cross-Correlation: ONI x Mauna Loa (oeni x mmlo)


__Plot and Save Figures__:
- Mauna Loa Auto-Correlation:
    - autocorr_mmlo.pdf
    - autocorr_mmlo_detail.pdf
- ONI Auto-Correlation:
    - autocorr_oeni.pdf
- Cross-Correlation: ONI x Mauna Loa (oeni x mmlo):
    - crosscorr_oeni_mmlo.pdf
    - crosscorr_oeni_mmlo_detail.pdf
    
### mlo_05_fft:

__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- FFT Calculations
- Mauna Loa FFT with Window Function only (no Zero-Padding)
- Mauna Loa FFT with Zero-Padding only
- Mauna Loa FFT with Zero-Padding and Window-Function
- Mauna Loa FFT with Zero-Padding + Window-Function (same Time-Range as ONI-Data)
- Oceanic Nino Index (ONI) FFT without Zeropadding / Window Function
- ONI FFT with Zero-Padding and Window-Function
- ONI FFT with Zero-Padding and Window-Function (same Time-Range as Mauna Loa-Data)


__Save Dataframes as Notebook Variables and as Text Files__:
- FFT Calculations:
    - fft_mmlo_nopad_nowin
- Mauna Loa FFT with Window Function only (no Zero-Padding):
    - fft_mmlo_onlywin_hann
    - fft_mmlo_onlywin_hamm
    - fft_mmlo_onlywin_black
    - fft_mmlo_onlywin_nuttall
    - fft_mmlo_onlywin_flattop
- Mauna Loa FFT with Zero-Padding only:
    - fft_mmlo_onlypad
- Mauna Loa FFT with Zero-Padding and Window-Function:
    - fft_mmlo
- Mauna Loa FFT with Zero-Padding + Window-Function (same Time-Range as ONI-Data):
    - fft_mmlo_cut_a 
- Oceanic Nino Index (ONI) FFT without Zeropadding / Window Function:
    - fft_oeni_nopad_nowin
- ONI FFT with Zero-Padding and Window-Function:
    - fft_oeni
- ONI FFT with Zero-Padding and Window-Function (same Time-Range as Mauna Loa-Data):
    - fft_oeni_cut_a

    
__Plot and Save Figures__:
- FFT Calculations:
    - fft_mmlo_nopad_nowin_bins.pdf
    - fft_mmlo_nopad_nowin_freq.pdf
    - fft_mmlo_nopad_nowin_years.pdf
- Mauna Loa FFT with Window Function only (no Zero-Padding):
    - fft_mmlo_onlywin.pdf
    - fft_mmlo_onlywin_detail.pdf
- Mauna Loa FFT with Zero-Padding only:
    - fft_mmlo_onlypad.pdf
    - fft_mmlo_win_pad_compare_a_detail.pdf
- Mauna Loa FFT with Zero-Padding and Window-Function:
    - fft_mmlo_win_pad_compare.pdf
    - fft_mmlo_compare.pdf
    - fft_mmlo_win_pad_compare_b.pdf
    - fft_mmlo_padwin.pdf
    - fft_mmlo_win_pad_compare_a.pdf
- ONI FFT with Zero-Padding and Window-Function:
    - fft_oeni_compare.pdf
 
 
 
### mlo_06-1_filter_mmlo:


__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Set Filter Settings
- Filter Response: Mauna Loa Unfiltered Data
- Filtering Time Domain Data
- Save Filtered Dataset


__Save Dataframes as Notebook Variables and as Text Files__:
- Save Filtered Dataset:
    - filtered_mmlo

    
__Plot and Save Figures__:
- Filter Response: Mauna Loa Unfiltered Data:
    - filter_response_years_fft_mmlo.pdf
    - filter_response_rad_fft_mmlo.pdf
    - filter_response_bins_fft_mmlo.pdf
- Filtering Time Domain Data:
    - filter_lowpass_filtered_mmlo.pdf
    - filter_highpass_filtered_mmlo.pdf
    - filter_butterworth_filtered_mmlo.pdf
        
        
### mlo_06-2_filter_oeni:

__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Set Filter Settings
- Filter Response: ONI Unfiltered Data
- Filtering Time Domain Data
- Save Filtered Dataset


__Save Dataframes as Notebook Variables and as Text Files__:
- Save Filtered Dataset:
    - filtered_oeni

    
__Plot and Save Figures__:
- Filter Response: ONI Unfiltered Data:
    - filter_response_years_fft_oeni.pdf
    - filter_response_rad_fft_oeni.pdf
    - filter_response_bins_fft_oeni.pdf
- Filtering Time Domain Data:
    - filter_lowpass_filtered_oeni.pdf
    - filter_highpass_filtered_oeni.pdf
    - filter_butterworth_filtered_oeni.pdf
    


### mlo_07_filtered_correlations_fft

__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Merge Filtered Time Series (Mauna Loa and ONI)
- Filtered Time Domain Signals: Mauna Loa- and ONI-Data
- Filtered Auto-Correlations
- Auto-Correlation - Mauna Loa and ONI
- Filtered Cross-Correlation: ONI x Mauna Loa
- FFT Calculations with Filtered Data
- Comparing Window Functions on Filtered Mauna Loa Data

__Save Dataframes as Notebook Variables and as Text Files__:
- Merge Filtered Time Series (Mauna Loa and ONI):
    - full_a_filtered
    - cut_a_filtered
- FFT Calculations with Filtered Data:
    - fft_filtered_mmlo
    - fft_filtered_mmlo_cut_a
    - fft_filtered_oeni
    - fft_filtered_oeni_cut_a

    
__Plot and Save Figures__:
- Filtered Time Domain Signals: Mauna Loa- and ONI-Data:
    - filtered_mmlo_oeni.pdf
- Filtered Auto-Correlations:
    - autocorr_mmlo_filtered.pdf
    - autocorr_oeni_filtered.pdf
- Auto-Correlation - Mauna Loa and ONI
    - autocorr_mmlo_oeni_unfiltered.pdf
    - autocorr_mmlo_oeni_filtered.pdf
- Filtered Cross-Correlation: ONI x Mauna Loa:
    - crosscorr_oeni_mmlo_filtered.pdf
    - crosscorr_oeni_mmlo_filtered_100_lags.pdf
    - crosscorr_oeni_mmlo_filtered_detail.pdf
- Comparing Window Functions on Filtered Mauna Loa Data:
    - fft_mmlo_filtered_win_compare.pdf    
        
        
        
### mlo_08_spectra_analysis:

__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Filtered FFT Results
- Create Result Tables of Filtered FFT Peaks in certain Time Periods


__Save Dataframes as Notebook Variables and as Text Files__:
- Create Result Tables of Filtered FFT Peaks in certain Time Periods:
    - fft_peaks_0_2_yr
    - fft_peaks_2_3_yr
    - fft_peaks_3_4_yr
    - fft_peaks_4_6_yr
    - fft_peaks_6_10_yr
    
    
- Merge Table Results of FFT Peaks
    - fft_peaks_merged
    - fft_peaks_merged_all
    - fft_peaks_years
    - fft_peaks_years_short

    
__Plot and Save Figures__:
- Filtered FFT Results:
    - fft_mmlo_filtered_compare
    - fft_mmlo_filtered_compare_norm
    - fft_mmlo_oeni_filtered
    - fft_mmlo_oeni_filtered_detail    
        
        
### mlo_09_synth_trend_prediction:

__Sections__:
- Main Module Import Section and Notebook Settings
- Initialize Custom Functions
- Read Notebook Variables
- Main Peaks of Filtered FFT Results in Time Period-Range of 2 - 6 Years: Mauna Loa and ONI
- Calculate Reconstructed Development of Atmospheric CO2-Concentrations
- Reconstructed Development of CO2-Concentrations without long-term Trend
- Reconstructed Development of CO2-Concentrations with long-term Trend


__Save Dataframes as Notebook Variables and as Text Files__:
- Create Dataframe with Reconstructed CO2-Trends:
    - synth
    - synth_future
    

__Plot and Save Figures__:
- Reconstructed Development of CO2-Concentrations without long-term Trend:
    - synth_mmlo_prog_detrended_noann
    - synth_mmlo_raw_detrended_noann_volc
    - synth_mmlo_prog_detrended_ann
- Reconstructed Development of CO2-Concentrations with long-term Trend:
    - synth_mmlo_prog
    - synth_mmlo_prog_volc
    - synth_mmlo_prog_detail
    - synth_mmlo_prog_noann
    - synth_mmlo_prog_noann_1980_2013_volc        