---
layout: page
title: Leaderboard
permalink: /leaderboard/
---

# Leaderboard

Below is the leaderboard showing accuracy scores on the held-out OOD datasets. Literature + Data outperforms all other methods in every model and task configuration. The bolded numbers outperform the few-shot method (*p < 0.05*), as determined by a paired t-test using five random seeds.

<script>
function toggleModel(model) {
  document.getElementById("gpt").style.display = (model === "gpt") ? "" : "none";
  document.getElementById("llama").style.display = (model === "llama") ? "" : "none";

  const gptLink = document.getElementById("gpt-link");
  const llamaLink = document.getElementById("llama-link");

  if (model === "gpt") {
    gptLink.style.fontWeight = "bold";
    llamaLink.style.fontWeight = "normal";
  } else {
    gptLink.style.fontWeight = "normal";
    llamaLink.style.fontWeight = "bold";
  }
}
</script>

<p>
  <a id="gpt-link" href="#" onclick="toggleModel('gpt'); return false;" style="font-weight: bold;">GPT-4-MINI</a> |
  <a id="llama-link" href="#" onclick="toggleModel('llama'); return false;">Llama-70B-I</a>
</p>

<table style="width: 95%; margin: auto; border-collapse: collapse; text-align: center; font-size: 0.95em;">
  <thead>
    <tr style="border-bottom: 2px solid black;">
      <!-- Removed Model column -->
      <th>Methods</th>
      <th>\deceptive</th>
      <th>\llamagc</th>
      <th>\gptgc</th>
      <th>\persuasion</th>
      <th>\dreaddit</th>
    </tr>
  </thead>

  <!-- GPT-4 MINI Section -->
  <tbody id="gpt">
    <tr>
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
    <tr>
      <td>Literature ∪ \hypogenic</td>
      <td>72.41</td>
      <td><b>83.00</b></td>
      <td><b>69.22</b></td>
      <td><b>89.88</b></td>
      <td>78.20</td>
    </tr>
    <tr>
      <td>Literature ∪ \refinemethod</td>
      <td>77.19</td>
      <td>55.33</td>
      <td>63.00</td>
      <td>89.52</td>
      <td><b>79.24</b></td>
    </tr>
  </tbody>

  <!-- Llama 70B-I Section -->
  <tbody id="llama" style="display: none;">
    <tr>
      <td colspan="6" style="font-weight: bold;">No hypothesis</td>
    </tr>
    <tr>
      <td>Zero-shot</td>
      <td>62.87</td>
      <td>58.67</td>
      <td>63.00</td>
      <td>85.60</td>
      <td>64.56</td>
    </tr>
    <tr>
      <td>Few-shot k=3</td>
      <td>68.56</td>
      <td>70.45</td>
      <td>76.00</td>
      <td>86.80</td>
      <td>69.44</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Zero-shot generation</td>
    </tr>
    <tr>
      <td>Zero-shot generation</td>
      <td>56.28</td>
      <td>50.67</td>
      <td>55.67</td>
      <td>88.16</td>
      <td>66.16</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Literature-based</td>
    </tr>
    <tr>
      <td>\paperonly</td>
      <td>64.25</td>
      <td>50.00</td>
      <td>49.67</td>
      <td>80.56</td>
      <td>66.04</td>
    </tr>
    <tr>
      <td>\hyperwrite</td>
      <td>58.62</td>
      <td>50.67</td>
      <td>54.00</td>
      <td>83.24</td>
      <td>74.40</td>
    </tr>
    <tr>
      <td>\notebooklm</td>
      <td>57.81</td>
      <td>49.33</td>
      <td>50.67</td>
      <td>67.64</td>
      <td>66.56</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Data-driven</td>
    </tr>
    <tr>
      <td>\hypogenic</td>
      <td>62.06</td>
      <td>78.67</td>
      <td>78.00</td>
      <td>88.44</td>
      <td>75.48</td>
    </tr>
    <tr>
      <td colspan="6" style="font-weight: bold;">Literature + Data (This work)</td>
    </tr>
    <tr>
      <td>\refinemethod</td>
      <td>72.16</td>
      <td>67.00</td>
      <td>66.67</td>
      <td>87.52</td>
      <td><b>78.92</b></td>
    </tr>
    <tr>
      <td>Literature ∪ \hypogenic</td>
      <td><b>73.72</b></td>
      <td><b>81.33</b></td>
      <td><b>78.67</b></td>
      <td>86.72</td>
      <td>72.56</td>
    </tr>
    <tr>
      <td>Literature ∪ \refinemethod</td>
      <td>71.75</td>
      <td>66.67</td>
      <td>65.67</td>
      <td><b>88.76</b></td>
      <td>74.80</td>
    </tr>
  </tbody>
</table>
