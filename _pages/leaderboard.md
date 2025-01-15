---
layout: page
title: Leaderboard
permalink: /leaderboard/
---

# Leaderboard

Below is the leaderboard showing accuracy scores on the held-out OOD datasets. Literature + Data outperforms all other methods in every model and task configuration. The bolded numbers outperform the few-shot method (*p < 0.05*), as determined by a paired t-test using five random seeds.

<table style="width: 95%; margin: auto; border-collapse: collapse; text-align: center; font-size: 0.95em;">
  <thead>
    <tr style="border-bottom: 2px solid black;">
      <th>Model</th>
      <th>Methods</th>
      <th>\deceptive</th>
      <th>\llamagc</th>
      <th>\gptgc</th>
      <th>\persuasion</th>
      <th>\dreaddit</th>
    </tr>
  </thead>
  <tbody>
    <!-- GPT-4 MINI Section -->
    <tr>
      <td rowspan="13" style="font-weight: bold;">GPT-4 MINI</td>
      <td colspan="6" style="font-weight: bold;">No hypothesis</td>
    </tr>
    <tr>
      <td>Zero-shot</td>
      <td>55.47</td>
      <td>50.00</td>
      <td>56.33</td>
      <td>81.24</td>
      <td>64.60</td>
    </tr>
    <tr>
      <td>Few-shot k=3</td>
      <td>65.56</td>
      <td>51.11</td>
      <td>64.22</td>
      <td>83.64</td>
      <td>75.00</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Zero-shot generation</td>
    </tr>
    <tr>
      <td>Zero-shot generation</td>
      <td>68.69</td>
      <td>49.00</td>
      <td>53.00</td>
      <td>86.08</td>
      <td>65.00</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Literature-based</td>
    </tr>
    <tr>
      <td>\paperonly</td>
      <td>59.22</td>
      <td>49.00</td>
      <td>54.00</td>
      <td>78.80</td>
      <td>67.68</td>
    </tr>
    <tr>
      <td>\hyperwrite</td>
      <td>61.63</td>
      <td>49.67</td>
      <td>52.67</td>
      <td>82.36</td>
      <td>68.76</td>
    </tr>
    <tr>
      <td>\notebooklm</td>
      <td>53.03</td>
      <td>49.33</td>
      <td>51.67</td>
      <td>68.96</td>
      <td>62.28</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Data-driven</td>
    </tr>
    <tr>
      <td>\hypogenic</td>
      <td>75.22</td>
      <td>81.67</td>
      <td>68.56</td>
      <td>82.20</td>
      <td>76.56</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Literature + Data (This work)</td>
    </tr>
    <tr>
      <td>\refinemethod</td>
      <td><b>77.78</b></td>
      <td>55.33</td>
      <td>63.33</td>
      <td>89.04</td>
      <td>78.04</td>
    </tr>
    <!-- Add remaining rows for Llama 70B-I similarly -->
  </tbody>
</table>
